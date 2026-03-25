Usage:
  exoram <command> [options]

Commands:
  run [options] <path>
  └──>  Run an application from RAM (via /dev/shm).
        This command handles copying, environment setup, and execution.

      Options:
        --no-rm           Do not remove working directory after exit
        --no-sync         Disable syncing changes back to source
        --no-env          Skip environment setup
        --from-existing   Use existing working directory in /dev/shm

  copy <source>
  └──>  Copy application to RAM workspace without executing

  setup <source>
  └──>  Prepare runtime environment (mock/overlay structure if needed)

  sync <pid> <source>
  └──>  Sync modified files back to source storage

  kill <pid>
  └──>  Terminate process and remove its RAM workspace

  cleanup
  └──>  Remove all ExoRAM working directories

  status
  └──>  Show running ExoRAM processes and their status


[[
A.B.C (Major.Minor.Patch)
Alpha, Beta, RC (Release Candidate)
exe:
]]

Version:
0.5-alpha {
    - Menambahkan command run untuk langsung menjalankan app dengan urutan lengkap
}

0.6-alpha {
    - Menambahkan command command yang dibutuhkan (status, run dengan option, sync, kill, cleanup)
    - Membuat app berjalan di background dan bisaa di kill ketika app tidak digunakan
    - Command status memberikan informasi tentang app apa saja yang ada di /dev/shm
}

Next Version:
0.7-alpha {
    - Menambahkan sistem pengecekan RAM
    - Memberikan peringatan yang jelas
    - Mengubah informasi ke bahassa inggris
    - Menyempurnakan sistem 
}


