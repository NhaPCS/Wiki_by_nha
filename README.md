# Wiki_by_nha
all things I always forget

## Host remotely
### Expose postgres port: 5432
```docker run --name posttest -d -p 5432:5432 -e POSTGRES_PASSWORD=dongbang009095 postgres:alpine```

### List all opening ports
```netstat -tulpn```

## Flutter build error:
- Firebase For Flutter Execution failed for task ':app:transformClassesWithDexForDebug': update gradle and google service

## Flutter build flavor
###IOS
```flutter run -d 350F9D48-A958-4551-88D5-21243897CB14 --flavor lop9_ios -t lib/main_lop9_ios.dart ```
