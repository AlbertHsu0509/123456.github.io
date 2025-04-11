---
layout: default
title: "Conditional Vocal Timbral Technique Conversion via Embedding-Guided Attribute Modulation"
---

<!-- Link to custom CSS to hide GitHub button and footer -->
<link rel="stylesheet" href="/assets/css/style.css">

## Abstract

Vocal timbral techniques—such as whisper, falsetto, and vocal fry/false cord scream—uniquely shape the spectral properties of the human voice, adding expressive nuance. Converting one timbral technique to another while preserving the original speaker’s identity remains a complex challenge. Traditional voice conversion methods excel at altering speaker identity or broad timbral qualities but often fail to accurately transform specialized timbral techniques without compromising speaker-specific traits. Similarly, existing style-transfer models, designed to capture emotional expressiveness or broad singing styles, lack the granularity and flexibility required to handle diverse, technique-specific timbral variations such as whisper or scream. To address this, we propose FABYOL, a novel embedding-guided framework for timbral technique conversion built upon a pre-trained, frozen FACodec architecture. FABYOL leverages supervised contrastive learning to generate robust embeddings that precisely encode individual timbral techniques, capturing their distinct spectral and stylistic features. Beyond timbre modulation, we emphasize prosody modulation as critical for achieving authentic conversions, employing adaptive layer normalization to modulate these attributes effectively during the transfer process. This approach enables precise, speaker-consistent transformations with minimal architectural changes. Through experimental evaluation—using tailored objective metrics and a user study—FABYOL demonstrates superior performance compared to state-of-the-art voice conversion models, advancing the fidelity and flexibility of timbral technique manipulation.

---
markdown

收起

換行

複製
---
layout: default
title: "Conditional Vocal Timbral Technique Conversion via Embedding-Guided Attribute Modulation"
---

<!-- Link to custom CSS to hide GitHub button and footer -->
<link rel="stylesheet" href="/assets/css/style.css">

## Abstract

Vocal timbral techniques—such as whisper, falsetto, and vocal fry/false cord scream—uniquely shape the spectral properties of the human voice, adding expressive nuance. Converting one timbral technique to another while preserving the original speaker’s identity remains a complex challenge. Traditional voice conversion methods excel at altering speaker identity or broad timbral qualities but often fail to accurately transform specialized timbral techniques without compromising speaker-specific traits. Similarly, existing style-transfer models, designed to capture emotional expressiveness or broad singing styles, lack the granularity and flexibility required to handle diverse, technique-specific timbral variations such as whisper or scream. To address this, we propose FABYOL, a novel embedding-guided framework for timbral technique conversion built upon a pre-trained, frozen FACodec architecture. FABYOL leverages supervised contrastive learning to generate robust embeddings that precisely encode individual timbral techniques, capturing their distinct spectral and stylistic features. Beyond timbre modulation, we emphasize prosody modulation as critical for achieving authentic conversions, employing adaptive layer normalization to modulate these attributes effectively during the transfer process. This approach enables precise, speaker-consistent transformations with minimal architectural changes. Through experimental evaluation—using tailored objective metrics and a user study—FABYOL demonstrates superior performance compared to state-of-the-art voice conversion models, advancing the fidelity and flexibility of timbral technique manipulation.

---

## Timbral Technique Conversion

To evaluate the performance of FABYOL and baseline models in the timbral technique conversion task, we randomly select samples from the test set featuring unseen singers as both reference and source. The source audio, in a modal voice, is conditioned on the reference audio to convert it to the target timbral technique.

<h2>🎵 Falsetto Conversion</h2>

<h3>Reference Files</h3>
<table class="reference-files">
  <thead>
    <tr>
      <th>Reference</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/falsetto/1/ref_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>

<h3>Model Comparisons</h3>
<table class="model-comparisons">
  <thead>
    <tr>
      <th>Source</th>
      <th>Ground Truth</th>
      <th>CosyVoice</th>
      <th>FreeVC</th>
      <th>FACodec</th>
      <th>FABYOL (Proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/falsetto/1/source_jvs021_parallel100_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/1/GT_jvs021_falset10_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/1/COSYjvs021_parallel100_VOICEACTRESS100_005_to_falsetto_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/1/Free_jvs021_parallel100_VOICEACTRESS100_005_to_falsetto_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/1/ORI_jvs021_parallel100_VOICEACTRESS100_005_to_falsetto_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/1/FABYOL_jvs021_parallel100_VOICEACTRESS100_005_to_falsetto_ref1_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="audio/conversion/falsetto/2/SOURCEjvs047_parallel100_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/2/GT_jvs047_falset10_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/2/COSYjvs047_parallel100_VOICEACTRESS100_001_to_falsetto_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/2/FREEjvs047_parallel100_VOICEACTRESS100_001_to_falsetto_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/2/ORI_jvs047_parallel100_VOICEACTRESS100_001_to_falsetto_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/falsetto/2/FABYOL_jvs047_parallel100_VOICEACTRESS100_001_to_falsetto_ref1_jvs001_falset10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>

<h2>🎵 Whisper Conversion</h2>

<h3>Reference Files</h3>
<table class="reference-files">
  <thead>
    <tr>
      <th>Reference</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/whisper/1/ref_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="audio/conversion/whisper/2/ref_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>

<h3>Model Comparisons</h3>
<table class="model-comparisons">
  <thead>
    <tr>
      <th>Source</th>
      <th>Ground Truth</th>
      <th>CosyVoice</th>
      <th>FreeVC</th>
      <th>FACodec</th>
      <th>FABYOL (Proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/whisper/1/source_jvs021_parallel100_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/1/GT_jvs021_whisper10_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/1/COSYjvs021_parallel100_VOICEACTRESS100_005_to_whisper_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/1/Free_jvs021_parallel100_VOICEACTRESS100_005_to_whisper_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/1/ORI_jvs021_parallel100_VOICEACTRESS100_005_to_whisper_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/1/FABYOL_jvs021_parallel100_VOICEACTRESS100_005_to_whisper_ref1_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="audio/conversion/whisper/2/SOURCEjvs047_parallel100_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/2/GT_jvs047_whisper10_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/2/COSYjvs047_parallel100_VOICEACTRESS100_001_to_whisper_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/2/FREEjvs047_parallel100_VOICEACTRESS100_001_to_whisper_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/2/ORI_jvs047_parallel100_VOICEACTRESS100_001_to_whisper_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/whisper/2/FABYOL_jvs047_parallel100_VOICEACTRESS100_001_to_whisper_ref1_jvs001_whisper10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>

<h2>🎵 Scream Conversion</h2>

<h3>Reference Files</h3>
<table class="reference-files">
  <thead>
    <tr>
      <th>Reference</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/scream/1/ref_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="audio/conversion/scream/2/ref_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>

<h3>Model Comparisons</h3>
<table class="model-comparisons">
  <thead>
    <tr>
      <th>Source</th>
      <th>Ground Truth</th>
      <th>CosyVoice</th>
      <th>FreeVC</th>
      <th>FACodec</th>
      <th>FABYOL (Proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/scream/1/source_jvs021_parallel100_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/1/GT_jvs021_scream10_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/1/COSYjvs021_parallel100_VOICEACTRESS100_005_to_scream_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/1/Free_jvs021_parallel100_VOICEACTRESS100_005_to_scream_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/1/ORI_jvs021_parallel100_VOICEACTRESS100_005_to_scream_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/1/FABYOL_jvs021_parallel100_VOICEACTRESS100_005_to_scream_ref1_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="audio/conversion/scream/2/SOURCEjvs047_parallel100_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/2/GT_jvs047_scream10_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/2/COSYjvs047_parallel100_VOICEACTRESS100_001_to_scream_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/2/FREEjvs047_parallel100_VOICEACTRESS100_001_to_scream_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/2/ORI_jvs047_parallel100_VOICEACTRESS100_001_to_scream_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/scream/2/FABYOL_jvs047_parallel100_VOICEACTRESS100_001_to_scream_ref1_jvs001_scream10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>

<h2>🎵 Modal Conversion</h2>

<h3>Reference Files</h3>
<table class="reference-files">
  <thead>
    <tr>
      <th>Reference</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/modal/1/ref_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="audio/conversion/modal/2/ref_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>

<h3>Model Comparisons</h3>
<table class="model-comparisons">
  <thead>
    <tr>
      <th>Source</th>
      <th>Ground Truth</th>
      <th>CosyVoice</th>
      <th>FreeVC</th>
      <th>FACodec</th>
      <th>FABYOL (Proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><audio controls src="audio/conversion/modal/1/source_jvs021_parallel100_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/1/GT_jvs021_modal10_VOICEACTRESS100_005.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/1/COSYjvs021_parallel100_VOICEACTRESS100_005_to_modal_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/1/Free_jvs021_parallel100_VOICEACTRESS100_005_to_modal_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/1/ORI_jvs021_parallel100_VOICEACTRESS100_005_to_modal_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/1/FABYOL_jvs021_parallel100_VOICEACTRESS100_005_to_modal_ref1_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="audio/conversion/modal/2/SOURCEjvs047_parallel100_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/2/GT_jvs047_modal10_VOICEACTRESS100_001.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/2/COSYjvs047_parallel100_VOICEACTRESS100_001_to_modal_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/2/FREEjvs047_parallel100_VOICEACTRESS100_001_to_modal_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/2/ORI_jvs047_parallel100_VOICEACTRESS100_001_to_modal_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
      <td><audio controls src="audio/conversion/modal/2/FABYOL_jvs047_parallel100_VOICEACTRESS100_001_to_modal_ref1_jvs001_modal10_BASIC5000_1635.wav"></audio></td>
    </tr>
  </tbody>
</table>
