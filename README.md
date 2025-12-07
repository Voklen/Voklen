👋Hello, I'm Alex
```Rust
pub fn main<'a>() -> Me<'a> {
	Me {
		name: "Alex Gorichev",
		uptime_years: 19,
		pronouns: vec!["he", "him"],
		favorite_languages: vec!["Rust", "Python", "GDScript"],
		software_preferences: SoftwarePreferences {
			os: "Arch linux",
			desktop_environment: "Hyprland",
			browser: "Firefox",
			search_engine: "Ecosia",
			editor: "Helix",
		},
	}
}

// Struct definitions

pub struct Me<'a> {
	name: &'a str,
	uptime_years: u64,
	pronouns: Vec<&'a str>, // Vector because pronouns could be added or removed during human's runtime
	favorite_languages: Vec<&'a str>,
	software_preferences: SoftwarePreferences<'a>,
}

pub struct SoftwarePreferences<'a> {
	os: &'a str,
	desktop_environment: &'a str,
	browser: &'a str,
	search_engine: &'a str, // Not local software, but software nevertheless
	editor: &'a str,
}
```

<!---
Voklen/Voklen is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
