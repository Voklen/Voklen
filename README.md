👋Hello, I'm Alex
```Rust
pub struct SoftwarePreferences<'a> {
	os: &'a str,
	desktop_environment: &'a str,
	browser: &'a str,
	search_engine: &'a str, // Not local software, but software nevertheless
	IDEs: Vec<&'a str>,
}

pub struct Me<'a> {
	name: &'a str,
	uptime: u128, // You never know...
	pronouns: Vec<&'a str>, // Vector because pronouns could be added or removed during human's runtime
	favorite_languages: Vec<&'a str>,
	software_preferences: SoftwarePreferences<'a>,
}

fn main() -> Me<'static> {
	Me {
		name: "Alex Gorichev",
		uptime: 17,
		pronouns: vec!["he", "him", "they", "them"],
		favorite_languages: vec!["Rust", "Python", "GDScript"],
		software_preferences: SoftwarePreferences {
			os: "Arch linux",
			desktop_environment: "Hyprland",
			browser: "Firefox",
			search_engine: "Ecosia",
			IDEs: vec!["Helix", "VSCodium"],
		},
	}
}
```

<!---
Voklen/Voklen is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
