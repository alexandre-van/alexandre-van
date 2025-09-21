## Hi there 👋

```c++
#include <string>
#include <vector>
#include <iostream>

class SoftwareDeveloper {
private:
    std::string fullName_;
    std::string nationality_;
    std::vector<std::string> languagesSpoken_;
    std::vector<std::string> programmingLanguages_;

public:
    SoftwareDeveloper() 
        : fullName_("Alexandre VAN")
        , nationality_("France")
        , languagesSpoken_({"French", "English"})
        , programmingLanguages_({"C", "C++", "React.js", "React-Native", "Django", "Go"}) {}

    void introduce() const {
        std::cout << "👋  Hello! I'm " << fullName_ << " from " << nationality_ << ".\n";
        printSkills("🗣️  I speak: ", languagesSpoken_);
        printSkills("💻  I code in: ", programmingLanguages_);
        std::cout << "🚀  Let's build something amazing together!\n";
    }

private:
    void printSkills(const std::string& prefix, const std::vector<std::string>& langs) const {
        std::cout << prefix;
        for (auto it = langs.begin(); it != langs.end(); ++it) {
            std::cout << *it;
            if (std::next(it) != langs.end()) {
                std::cout << (std::next(it, 2) == langs.end() ? " and " : ", ");
            }
        }
        std::cout << "\n";
    }
};

int main() {
    SoftwareDeveloper me;
    me.introduce();
    return 0;
}
```

<!--
**alexandre-van/alexandre-van** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
