<!-- # CanvasToPdf.vue

<template>
  <div>
    <canvas ref="canvasElement"></canvas>
    <button @click="convertToPdf">Convert to PDF</button>
  </div>
</template>

<script>
import html2canvas from 'html2canvas';
import jsPDF from 'jspdf';

export default {
  methods: {
    convertToPdf() {
      const canvasElement = this.$refs.canvasElement;

      html2canvas(canvasElement).then(canvas => {
        const imgData = canvas.toDataURL('image/png');
        const pdf = new jsPDF();
        pdf.addImage(imgData, 'PNG', 0, 0);
        pdf.save('canvas.pdf');
      });
    }
  }
}
</script> -->



<template>
    <div>
      <canvas ref="canvasElement" width="400" height="400"></canvas>
      <button @click="convertToPdf">Convert to PDF</button>
    </div>
  </template>
  
  <script>
  import html2canvas from 'html2canvas';
  import jsPDF from 'jspdf';
  
  export default {
    methods: {
      convertToPdf() {
        const canvasElement = this.$refs.canvasElement;
  
        html2canvas(canvasElement).then(canvas => {
          const imgData = canvas.toDataURL('image/png');
          const pdf = new jsPDF();
          pdf.addImage(imgData, 'PNG', 0, 0);
          pdf.save('canvas.pdf');
        });
      }
    }
  }
  </script>
  
  <style scoped>
  canvas {
    border: 1px solid black;
  }
  </style>
  