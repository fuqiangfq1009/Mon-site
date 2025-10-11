    <h1>Contactez-moi</h1>
    <p>Je suis toujours là pour vous aider à planifier votre voyage en Chine. N'hésitez pas à m'envoyer un message !</p>
    
    <div class="contact-grid" style="display: flex; flex-wrap: wrap; justify-content: space-around; gap: 30px; margin-top: 40px; text-align: left;">
        
        <div style="flex: 1; min-width: 300px; max-width: 450px; padding: 20px; border: 1px solid #ddd; border-radius: 8px; background-color: #f9f9f9;">
            <h2>Informations de contact</h2>
            <div style="display: flex; align-items: center; margin-bottom: 20px; border-bottom: 1px solid #eee; padding-bottom: 15px;">
                <div>
                    <h3 style="color: #c00; margin-bottom: 5px;">FU Qiang</h3>
                    <p style="color: #555; font-size: 16px;">Créateur du site / Guide</p>
                </div>
            </div>
            
            <p style="margin-bottom: 15px;"><strong style="color: #c00;">Email :</strong> voyage.chine.contact@email.com</p>
            <p style="margin-bottom: 15px;"><strong style="color: #c00;">Téléphone :</strong> +33 7 00 00 00 00</p>
            <p style="margin-bottom: 20px;"><strong style="color: #c00;">Adresse :</strong> UBO, 3, rue Matthieu-Gallou, 29238 Brest Cedex 3</p>
            
            <h3 style="color: #c00; margin-top: 30px;">Suivez-nous !</h3>
            <img src="<img width="259" height="194" alt="image" src="https://github.com/user-attachments/assets/5376c76e-0da4-42f2-a802-09611626f08e" />
" alt="QR Code" style="width: 120px; height: 120px; display: block; margin-top: 15px; border: 1px solid #c00;">
Scannez pour m'ajouter sur WhatsApp.
        
        <div style="flex: 1; min-width: 300px; max-width: 600px; padding: 20px; border: 1px solid #ddd; border-radius: 8px; background-color: #fff;">
            <h2>Envoyez-nous un message rapide</h2>
            <form onsubmit="event.preventDefault(); showConfirmation();" style="display: flex; flex-direction: column; gap: 15px;">
                <label for="name" style="font-weight: bold; color: #333;">Votre Nom :</label>
                <input type="text" id="name" name="name" required placeholder="Ex: Jean Dupont" style="padding: 10px; border: 1px solid #ccc; border-radius: 4px; font-size: 16px;">
                
                <label for="message" style="font-weight: bold; color: #333;">Votre Message :</label>
                <textarea id="message" name="message" rows="6" required placeholder="Comment pouvons-nous vous aider ? (Ex: Je cherche un circuit de 10 jours à Pékin.)" style="padding: 10px; border: 1px solid #ccc; border-radius: 4px; resize: vertical; font-size: 16px;"></textarea>
                
                <button type="submit" class="btn" style="align-self: flex-start; margin-top: 10px; /* Réutilise le style du bouton principal */">
                    Envoyer le Message
                </button>
            </form>
            
            <p id="confirmation-message" style="margin-top: 20px; color: green; font-weight: bold; text-align: center; display: none;">Message envoyé avec succès ! Nous vous répondrons bientôt.</p>
        </div>
    </div>
</div>

<style>
    /* Styles spécifiques pour la page Contact, pour assurer l'alignement */
    #content-area {
        text-align: left !important; /* Pour que le contenu du contact ne soit pas centré */
        padding: 40px 60px !important;
    }
    .contact-page h1 {
        text-align: center;
        margin-bottom: 10px;
    }
    .contact-page p {
        text-align: center;
        margin-bottom: 25px;
        font-size: 18px;
    }
    .contact-page h2 {
        color: #c00;
        margin-bottom: 20px;
        text-align: center;
        font-size: 26px;
    }
</style>

<script>
    function showConfirmation() {
        // En conditions réelles, vous enverriez les données à un serveur ici.
        
        // Simuler l'envoi et afficher la confirmation
        document.getElementById('confirmation-message').style.display = 'block';
        
        // Optionnel : Effacer les champs après un court délai
        setTimeout(() => {
            document.getElementById('name').value = '';
            document.getElementById('message').value = '';
            document.getElementById('confirmation-message').style.display = 'none';
        }, 3000);
    }
</script>
