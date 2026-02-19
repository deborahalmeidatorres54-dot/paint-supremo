self.addEventListener("install", event => {
  event.waitUntil(
    caches.open("paint-cache").then(cache => {
      return cache.addAll([
        "paint.html",
        "manifest.json"
      ]);
    })
  );
});
