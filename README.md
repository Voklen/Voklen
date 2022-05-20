👋Hello, I'm Alex
```Rust
pub struct SoftwarePreferences<'a> {
	os: &'a str,
	desktop_environment: &'a str,
	browser: &'a str,
	search_engine: &'a str, // Not local software, but software nevertheless
	IDE: &'a str,
}

pub struct Me<'a> {
	name: &'a str,
	uptime: u128, // You never know...
	pronouns: (&'a str, &'a str),
	favorite_languages: Vec<&'a str>, // Vector because languages could be added during human's runtime
	software_preferences: SoftwarePreferences<'a>,
}

fn main() -> Me<'static> {
	Me {
		name: "Alex Gorichev",
		uptime: 15,
		pronouns: ("he", "him"),
		favorite_languages: vec!["Rust", "Python", "GDScript"],
		software_preferences: SoftwarePreferences {
			os: "Arch linux",
			desktop_environment: "KDE",
			browser: "Firefox",
			search_engine: "Ecosia",
			IDE: "VSCodium",
		},
	}
}


```

<!---
Voklen/Voklen is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
