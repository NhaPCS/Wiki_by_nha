# Wiki_by_nha
all things I always forget

## Host remotely
### Expose postgres port: 5432
```docker run --name posttest -d -p 5432:5432 -e POSTGRES_PASSWORD=dongbang009095 postgres:alpine```

### List all opening ports
```netstat -tulpn```

## Flutter build error:
- Firebase For Flutter Execution failed for task ':app:transformClassesWithDexForDebug': update gradle and google service

