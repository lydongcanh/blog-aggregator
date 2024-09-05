# Blog Aggregator API

[![Build Status](https://github.com/lydongcanh/blog-aggregator/actions/workflows/ci.yml/badge.svg)](https://github.com/lydongcanh/yawndb/actions/workflows/ci.yml)

This is the backend API for the Blog Aggregator application, built using **ASP.NET Core Web API**. It fetches blog posts from external sources (such as Netflix, Uber, etc.) and serves them via a REST API that the frontend React application consumes.

## Features

- Fetches blog posts from multiple external sources.
- Exposes REST API endpoints for the frontend to consume.
- Uses `HttpClient` to retrieve RSS feeds and `SyndicationFeed` to parse them.

## Prerequisites

- [.NET SDK 8+](https://dotnet.microsoft.com/download)
- [RSS feed URLs](https://en.wikipedia.org/wiki/List_of_RSS_feeds) from blogs you want to aggregate.

## Getting Started

1. **Clone the repository**:
```bash
git clone https://github.com/yourusername/BlogAggregatorAPI.git
cd BlogAggregatorAPI
```

2. **Install dependencies** (if any):
```bash
dotnet restore
```

3. **Add RSS feeds**: Add the URLs of the RSS feeds you want to aggregate in BlogService.

4. Run the application:
```bash
dotnet run
```

5. **API Endpoints**:
```
GET /api/blogs - Fetch all blog posts from aggregated sources.
```

### Sample Response
```json
[
  {
    "title": "Building Scalable Systems",
    "author": "John Doe",
    "publishedDate": "2024-09-01T10:00:00Z",
    "content": "This is a sample blog post from an external source...",
    "sourceUrl": "https://example.com/blog/building-scalable-systems"
  }
]
```