
# Latihan1_AplikasiPertambahanDuaAngka  
**Nama**: [Irfazi]  
**NPM**: [2210010277]

---

## Deskripsi Program  
- **Pengguna memasukkan dua angka**.  
- **Saat tombol Tambah diklik**, hasil pertambahan akan ditampilkan.  
- **Saat tombol Hapus diklik**, semua nilai akan dihapus, dan fokus kembali ke TextField angka pertama.  
- **Saat tombol Keluar diklik**, aplikasi akan ditutup.  

---

## Komponen GUI: JFrame, JPanel, JLabel, JTextField, JButton  
- **JLabel**: Memberikan label pada input angka pertama, angka kedua, dan hasil.  
- **JTextField**: Digunakan untuk memasukkan angka pertama, angka kedua, dan menampilkan hasil.  
- **JButton**:  
  - **Tambah**: Melakukan operasi penjumlahan.  
  - **Hapus**: Menghapus semua input.  
  - **Keluar**: Menutup aplikasi.  

---

## Logika Program  
Aplikasi menangani operasi penjumlahan dua angka dengan validasi input numerik.  

---

## Events  
### A. **Tambah**  

```java
private void btnTambahActionPerformed(java.awt.event.ActionEvent evt) {                                          
    try {
        int angka1 = Integer.parseInt(txtAngka1.getText());
        int angka2 = Integer.parseInt(txtAngka2.getText());
        int hasil = angka1 + angka2;
        txtHasil.setText(String.valueOf(hasil));
    } catch (NumberFormatException e) {
        JOptionPane.showMessageDialog(this, "Masukkan angka yang valid!", "Error", JOptionPane.ERROR_MESSAGE);
    }
}
```  

### B. **Hapus**  

```java
private void btnHapusActionPerformed(java.awt.event.ActionEvent evt) {                                         
    txtAngka1.setText("");
    txtAngka2.setText("");
    txtHasil.setText("");
    txtAngka1.requestFocus();
}
```  

### C. **Keluar**  

```java
private void btnKeluarActionPerformed(java.awt.event.ActionEvent evt) {                                          
    System.exit(0);
}
```  

---

## Variasi  
### A. **KeyAdapter** pada JTextField untuk membatasi input hanya angka:  

```java
private void txtAngka1KeyTyped(java.awt.event.KeyEvent evt) {                                           
    char c = evt.getKeyChar();
    if (!Character.isDigit(c)) {
        evt.consume();
        JOptionPane.showMessageDialog(this, "Masukkan hanya angka!", "Error", JOptionPane.ERROR_MESSAGE);
    }
}
```  

### B. Gunakan **JOptionPane** untuk menangani error input:  

```java
} catch (NumberFormatException e) {
    JOptionPane.showMessageDialog(this, "Input harus berupa angka!", "Error", JOptionPane.ERROR_MESSAGE);
}
```  

### C. **FocusListener** untuk membersihkan JTextField saat fokus didapatkan:  

```java
private void txtAngka1FocusGained(java.awt.event.FocusEvent evt) {                                              
    txtAngka1.setText("");
    txtAngka2.setText("");
}
```  

---

## Hasil Gambar Project Ketika di Run  
![Screenshot Aplikasi](https://github.com/[username]/Latihan1_AplikasiPertambahanDuaAngka/blob/main/screenshot.png)  

---

## Indikator Penilaian  

| No  | Komponen         | Persentase |
| :-: | --------------   |   :-----:  |
|  1  | Komponen GUI     |    20%     |
|  2  | Logika Program   |    20%     |
|  3  | Events           |    15%     |
|  4  | Kesesuaian UI    |    15%     |
|  5  | Memenuhi Variasi |    30%     |
|     | **TOTAL**        |  100%      |  

---

## Pembuat  

**Nama**: [Irfazi]  
**NPM**: [2210010277]  

--- 
