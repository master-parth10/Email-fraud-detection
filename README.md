# Login Page
# -------------------------------

tk.Label(
    login_frame,
    text="Email Fraud Detection",
    font=("Arial", 24, "bold"),
    bg="#1e1e2f",
    fg="white"
).pack(pady=30)

tk.Label(
    login_frame,
    text="Username",
    bg="#1e1e2f",
    fg="white",
    font=("Arial", 14)
).pack()

user_entry = tk.Entry(login_frame, font=("Arial", 14))
user_entry.pack(pady=10)

tk.Label(
    login_frame,
    text="Password",
    bg="#1e1e2f",
    fg="white",
    font=("Arial", 14)
).pack()

pass_entry = tk.Entry(login_frame, show="*", font=("Arial", 14))
pass_entry.pack(pady=10)

tk.Button(
    login_frame,
    text="Login",
    font=("Arial", 14),
    bg="#4CAF50",
    fg="white",
    command=login
).pack(pady=20)

# -------------------------------
# Detector Page
# -------------------------------

tk.Label(
    detector_frame,
    text="Enter Email Content",
    font=("Arial", 22, "bold"),
    bg="#1e1e2f",
    fg="white"
).pack(pady=20)

email_box = tk.Text(
    detector_frame,
    height=12,
    width=60,
    font=("Arial", 12)
)
email_box.pack(pady=20)

tk.Button(
    detector_frame,
    text="Detect Fraud",
    font=("Arial", 14),
    bg="#2196F3",
    fg="white",
    command=detect_email
).pack()
# Result Page
# -------------------------------

tk.Label(
    result_frame,
    text="Detection Result",
    font=("Arial", 24, "bold"),
    bg="#1e1e2f",
    fg="white"
).pack(pady=40)

result_label = tk.Label(
    result_frame,
    text="",
    font=("Arial", 28, "bold"),
    bg="#1e1e2f"
)

result_label.pack(pady=30)

tk.Button(
    result_frame,
    text="Scan Another Email",
    font=("Arial", 14),
    bg="#FF9800",
    fg="white",
    command=show_detector
).pack(pady=20)

# -------------------------------
# Start App
# -------------------------------

show_login()

root.mainloop()
