# MongoDB Backup Job on Kubernetes 🛠️📦  

This repository provides a setup for running a **MongoDB backup job** on a Kubernetes cluster. It includes configurations for **persistent volumes (PV)**, **persistent volume claims (PVC)**, and **Kubernetes jobs** to automate the backup process.

---

## Features ✨  

- **Automated Backup**: Scheduled backups of MongoDB databases.  
- **Kubernetes Native**: Uses Kubernetes Jobs, PV, and PVC for efficient backup storage.  
- **Scalable**: Easily adaptable to different MongoDB setups.  

---

## Prerequisites 🛠️  

- A running Kubernetes cluster.  
- Kubernetes CLI (`kubectl`) configured.  
- MongoDB instance accessible from the cluster.  

---

## Installation  

1. Clone the repository:  
git clone https://github.com/your-username/mongo_backup_job.git  
cd mongo_backup_job  

2. Apply the persistent volume and claim:  
kubectl apply -f pv.yaml  
kubectl apply -f pvc.yaml  

3. Apply the MongoDB backup job:  
kubectl apply -f backup-job.yaml  

---

## Configuration  

- **PV and PVC**: Update `pv.yaml` and `pvc.yaml` to define storage size and access modes.  
- **Job File**: Modify `backup-job.yaml` to set MongoDB connection details and backup frequency.  

---

## Monitoring  

1. Check the status of the backup job:  
kubectl get jobs  

2. View logs for troubleshooting:  
kubectl logs <backup-job-pod-name>  

3. Verify backups in the persistent storage.  

---

## File Structure 📂  

- `pv.yaml`: Persistent Volume configuration.  
- `pvc.yaml`: Persistent Volume Claim configuration.  
- `backup-job.yaml`: Kubernetes Job for MongoDB backup.  
- `README.md`: Documentation for the repository.  

---

## Example Commands  

- Apply PV and PVC:  
  kubectl apply -f pv.yaml  
  kubectl apply -f pvc.yaml  

- Run the backup job:  
  kubectl apply -f backup-job.yaml  

- Check job logs:  
  kubectl logs <backup-job-pod-name>  

---

## Contributing 🤝  

1. Fork the repository.  
2. Create a new branch:  
git checkout -b feature/your-feature  

3. Commit your changes:  
git commit -m "Add your feature"  

4. Push the branch:  
git push origin feature/your-feature  

5. Open a pull request.  

---

## License 📝  

This project is licensed under the MIT License. See the LICENSE file for details.  

---

**Easily manage MongoDB backups with Kubernetes Jobs!** 🛠️📦  
