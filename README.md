# sent
no
// sau khi chạy xong N-1 vòng lặp Bellman-Ford 
for(int T = 0; T < n; T++){
    for (auto E : e) {
        int u = E.u;
        int v = E.v;
        long long w = E.w;
        if (D[u] != INF && D[v] > D[u] + w) {
            // vẫn còn tối ưu được --> âm vô cực
            D[v] = -INF;
            trace[v] = u;
        }
    }
}
