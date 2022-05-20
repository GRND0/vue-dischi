<template>
    <div>
        <div>
            <label for="selettore-genere">Filtra per genere</label>

            <select v-model="selezione" @change="$emit('opzione', selezione)" id="selettore-genere">
                <option value="">Tutti i generi</option>
                <option value="Rock">Rock</option>
                <option value="Pop">Pop</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
            </select>
        </div>

        <div>
            <label for="selettore-artista">Filtra per artista</label>

            <select v-model="selezioneArtista" @change="$emit('opzioneArtista', selezioneArtista)"
                id="selettore-artista">
                <option value="">Tutti gli artisti</option>
                <option value="Bon Jovi">Bon Jovi</option>
                <option value="Queen">Queen</option>
                <option value="Sting">Sting</option>
                <option value="Steve Gadd Band">Steve Gadd Band</option>
                <option value="Iron Maiden">Iron Maiden</option>
                <option value="Deep Purple">Steve Gadd Band</option>
                <option value="Metallica">Metallica</option>
                <option value="Dave Weckl">Dave Weckl</option>
                <option value="Michael Jacjson">Michael Jacjson</option>
            </select>
        </div>
    </div>
</template>

<script>
export default {
    name: "CustomSelettore",
    data: function () {
        return {
            selezione: "",
            selezioneArtista: "",
        };
    },
};
</script>

<style>
</style>
