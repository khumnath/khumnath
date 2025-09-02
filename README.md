 🧑‍💻 khumnath — g++ -std=c++17 profile.cpp -o profile && ./profile



```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;
string binaryToString(const string& b) {
    string r;
    for (size_t i = 0; i < b.size(); i += 8)
        r.push_back(char(stoi(b.substr(i, 8), nullptr, 2)));
    return r;
}
struct Profile {
    string os, shell, device, website, country, email_bin;
    vector<string> languages;
};
ostream& operator<<(ostream& o, const Profile& p) {
    o << p.os << "\n" << p.shell << "\n" << p.device << "\n"
      << p.website << "\n" << p.country << "\n"
      << "Email: 📧 " << binaryToString(p.email_bin) << "\nLanguages: ";
    for (auto& l : p.languages) o << l << " ";
    return o;
}

int main() {
    Profile me = {
        "🖥️  Deepin 25",
        "🐚  bash",
        "💻  Lenovo Ideapad Pro 5i",
        "🌐  https://khumnath.com.np",
        "🇳🇵  Nepal",        "0110111001100001011101000110100000101110011010110110100001110101011011010110111001100001011101000110100001000000011001110110110101100001011010010110110000101110011000110110111101101101",
        {"Javascript", "Typescript", "QML", "C++", "Python"}
    };
    cout << me << "\n";
}
```
| ![khumnath's Stats](https://github-readme-stats.vercel.app/api?username=khumnath&theme=merko&show_icons=true&hide_border=false&count_private=true) | ![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=khumnath&hide=css,scss,html&theme=merko&show_icons=true&layout=compact) |
|--|--|

![khumnath's Streak](https://github-readme-streak-stats.herokuapp.com/?user=khumnath&theme=merko&hide_border=false)

