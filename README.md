# Vercel Blog 만들기 

## Vercle blog Starter Kit 
https://vercel.com/templates/next.js/blog-starter-kit   
위의 링크로 접속하여 

`npx create-next-app --example blog-starter blog-starter-app`   

설치해준다. 

`npm run dev`   
로 제대로 출력되는지 확인한다. 

루트 파일에 `next.config.js` 파일을 만든 뒤     
```javascript
/**
 * @type {import('next').NextConfig}
 */
const nextConfig = {
    output: 'export',
    distDir: 'dist',
    images: {
        unoptimized: true
    }
}

module.exports = nextConfig

``` 
을 입력해준다.  

이후 `npm run build`를 사용해 build해준다. 

build 한 뒤 `npx serve ./dist`를 실행하면, 

```

   ┌───────────────────────────────────────────┐
   │                                           │
   │   Serving!                                │
   │                                           │
   │   - Local:    http://localhost:3000       │
   │   - Network:  http://192.168.0.101:3000   │
   │                                           │
   │   Copied local address to clipboard!      │
   │                                           │
   └───────────────────────────────────────────┘

```

이런 내용이 뜨면 성공이다.  

이후 새 리퍼스토리를 만들어 깃해준다. 

