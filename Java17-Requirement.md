# 🛠️ Setup Java 17 and Maven on Ubuntu 24.04

This guide helps you completely remove existing Java and Maven installations and reinstall Java 17 and Maven cleanly on Ubuntu 24.04.

---

## 📦 Step 1: Remove Existing Java and Maven

```bash
sudo apt remove --purge openjdk* maven -y
sudo apt autoremove --purge -y
sudo rm -rf /usr/lib/jvm/*
sudo rm -rf ~/.m2

## Install JDK

sudo apt update
sudo apt install openjdk-17-jdk -y

## Set Java 17 as default:

sudo update-alternatives --config java
sudo update-alternatives --config javac

## verify
java -version    # openjdk version "17..."
javac -version   # javac 17...


