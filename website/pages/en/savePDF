
printPDF.then(pdf => {
	res.set({ 'Content-Type': 'application/pdf', 'Content-Length': pdf.length })
	res.send(pdf)
  function getPDF() {
 return axios.get(`${API_URL}/your-pdf-endpoint`, {
   responseType: 'arraybuffer',
   headers: {
     'Accept': 'application/pdf'
   }
 })
 savePDF = () => {
    this.openModal(‘Loading…’) // open modal
   return getPDF() // API call
     .then((response) => {
       const blob = new Blob([response.data], {type: 'application/pdf'})
       const link = document.createElement('a')
       link.href = window.URL.createObjectURL(blob)
       link.download = `your-file-name.pdf`
       link.click()
       this.closeModal() // close modal
     })
   .catch(err => /** error handling **/)
 }
          
<button onClick={this.savePDF}>Save as PDF</button>  
