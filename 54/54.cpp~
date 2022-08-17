#include <bits/stdc++.h>
#define rep(i, l, r) for (int i = l; i <= r; i++)
#define per(i, r, l) for (int i = r; i >= l; i--)
#define srep(i, l, r) for (int i = l; i < r; i++)
#define sper(i, r, l) for (int i = r; i > l; i--)
#define erep(i, x) for (int i = h[x]; i; i = e[i].next)
#define erep2(i, x) for (int& i = cur[x]; i; i = e[i].next)
#define pii pair<int, int>
#define pll pair<ll, ll>
#define pdd pair<double, double>
#define fi first
#define se second
#define ui unsigned int
#define ld long double
#define pb push_back
#define pc putchar
#define vi vector<int> 
#define lowbit(x) (x & -x)
#define maxbuf 2000020
#define gc() ((p1 == p2 && (p2 = (p1 = buffer) + fread(buffer, 1, maxbuf, stdin), p1 == p2)) ? EOF : *p1++)
using namespace std;

namespace Fast_Read{
    char buffer[maxbuf], *p1, *p2;
    template<class T> void read_signed(T& x){
        char ch = gc(); x = 0; bool f = 1;
        while (!isdigit(ch) && ch != '-') ch = gc();
        if (ch == '-') f = 0, ch = gc();
        while ('0' <= ch && ch <= '9') x = (x << 1) + (x << 3) + ch - '0', ch = gc();
        x = (f) ? x : -x;
    }
    template<class T, class... Args> void read_signed(T& x, Args&... args){
        read_signed(x), read_signed(args...);
    }
    template<class T> void read_unsigned(T& x){
        char ch = gc(); x = 0;
        while (!isdigit(ch)) ch = gc(); 
        while (isdigit(ch)) x = (x << 1) + (x << 3) + ch - '0', ch = gc(); 
    }
    template<class T, class... Args> void read_unsigned(T& x, Args&... args){
        read_unsigned(x), read_unsigned(args...);
    }
    #define isletter(ch) ('0' <= ch && ch <= '9' || 'A' <= ch && ch <= 'Z')
    int read_string(char* s){
        char ch = gc(); int l = 0;
        while (!isletter(ch)) ch = gc();
        while (isletter(ch)) s[l++] = ch, ch = gc();
        s[l] = '\0'; return l;
    }
}using namespace Fast_Read; 

int _num[20];
template <class T> void write(T x, char sep = '\n'){	
	if (!x) {putchar('0'), putchar(sep); return;}
	if (x < 0) putchar('-'), x = -x;
	int c = 0;
	while (x) _num[++c] = x % 10, x /= 10;
	while (c) putchar('0' + _num[c--]); 
	putchar(sep);
}

#define read read_signed
#define reads read_string 
#define writes puts

#define maxn
#define maxm
#define maxs
#define maxb
#define inf 
#define eps
#define M 
#define ll long long int 

vector<vi> carda, cardb;

int value(char ch) {
	if (isdigit(ch)) return ch - '0';
	switch(ch){
		case 'A': return 1;
		case 'T': return 10;
		case 'J': return 11;
		case 'Q': return 12;
		case 'K': return 13;
	}
	assert(false); 
}

int suit(char ch) {
	switch(ch){
		case 'D': return 1;
		case 'C': return 2;
		case 'H': return 3;
		case 'S': return 4;
	}
	assert(false);
}

vi RoyalFlush(vector<vi>& card) {
	rep(s, 1, 4) if (card[s][10] && card[s][11] && card[s][12] && card[s][13] && card[s][1]) {
		card[s][10] = card[s][11] = card[s][12] = card[s][13] = card[s][1] = 0;
		return vi{10}; 
	} return vi{-1};
}

int StraightFlush(vector<vi>& card) {	
	rep(s, 1, 4) rep(v, 1, 9) {
		rep(i, 0, 4) if (!card[s][v + i]) goto fail1; 
		rep(i, 0, 4) card[s][v + i] = 0;
		return v;
		fail1:; 
	} return -1;
}

int FourofaKind(vector<vi>& card) {
	rep(v, 1, 13) {
		rep(s, 1, 4) if (!card[s][v]) goto fail2;  
		rep(s, 1, 4) card[s][v] = 0;
		return v;
		fail2:;
	} return -1;
}

int FullHouse(vector<vi>& card) {
	
}

bool Flush(vector<vi>& card) {

}

bool Straight(vector<vi>& card) {

}

bool ThreeofaKind(vector<vi>& card) {
	
}

bool TwoPairs(vector<vi>& card) {
	
}

bool OnePair(vector<vi>& card) {
	
}

bool HighCard(vector<vi>& card) {
	
}

bool empty(vector<vi>& card) {
	rep(s, 1, 4) if (!card[s].empty()) return false; return true;
}

int comp(vector<vi>& carda, vector<vi>& cardb) {
	
}

void init(vector<vi>& carda, vector<vi>& cardb) {
	carda.clear(),   cardb.clear();
	carda.resize(5), cardb.resize(5);
	for (auto it: carda) it.resize(14);
	for (auto it: cardb) it.resize(14);
}

void work(){
	int cnt = 0;
	rep(i, 1, 1000) {
		vector<vi> carda, cardb;
		init(carda, cardb);
		char s[5];
		rep(j, 1, 5) {
			reads(s + 1);
			carda[suit(s[2])][value(s[1])]++;
		}
		rep(j, 1, 5) {
			reads(s + 1);
			cardb[suit(s[2])][value(s[1])]++;
		}
		if (comp(carda, cardb) > 0) cnt++;
	}
	printf("%d\n", cnt);
}

int main(){ work(); return 0; }

