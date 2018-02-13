<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. tryte</a></li>
<li><a href="#sec-2">2. bookmarks</a></li>
<li><a href="#sec-3">3. transaction</a></li>
<li><a href="#sec-4">4. generate iota seed</a></li>
<li><a href="#sec-5">5. address</a></li>
</ul>
</div>
</div>

# tryte<a id="sec-1" name="sec-1"></a>

1 byte = 8 bits = 256 (2<sup>8</sup>) combinations
1 tryte = 3 trits = 27 (3<sup>3</sup>) combinations
2 trytes = 6 trits = 729 (3<sup>6</sup>) combinations
1 byte + padding = 2 trytes
padding = 729 - 256 = 473 combinations

# bookmarks<a id="sec-2" name="sec-2"></a>

browser - <http://open-iota.prizziota.com/#/>
chatangle - <https://www.chatangle.com/#/>
MAM - <https://blog.iota.org/introducing-masked-authenticated-messaging-e55c1822d50e>
forum for developers - <https://forum.helloiota.com/Technology/Developers>

python - <https://github.com/iotaledger/iota.lib.py>

cryptography
<https://github.com/jedisct1/libsodium>
caesium - <https://github.com/lvh/caesium>
sha-3 <https://en.wikipedia.org/wiki/SHA-3>
keccak - <https://keccak.team/index.html>

<http://iota.dance/live/>
browser - <https://thetangle.org/>
explorer - <http://tangle.glumb.de/>

CarrIOTA Field: Node intel and balancing - <https://medium.com/deviota/carriota-field-node-intel-and-balancing-223002156b54>

tryte decoder/encoder - <https://iota.felixseele.de/>
convert - <https://laurencetennant.com/iota-tools/>
iota convertors: <https://laurencetennant.com/iota-tools/>

playbook - <http://iri-playbook.readthedocs.io/en/master/index.html>
partners - <http://iota.partners/>
aws - <https://github.com/iotFab/iota-aws-full-node>

docs - <https://iota.readme.io/docs>
kerl/curl - <https://github.com/iotaledger/kerl>
kerl spec - <https://github.com/iotaledger/kerl/blob/master/IOTA-Kerl-spec.md>
sim - <https://simulation1.tangle.works/>
transaction how? - <https://medium.com/@louielu/in-depth-explanation-of-how-iota-making-a-transaction-with-picture-8a638805f905>

# transaction<a id="sec-3" name="sec-3"></a>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">Field</th>
<th scope="col" class="left">Type</th>
<th scope="col" class="right">#trytes</th>
</tr>
</thead>

<tbody>
<tr>
<td class="left">address</td>
<td class="left">String</td>
<td class="right">27</td>
</tr>


<tr>
<td class="left">attachmentTimestamp</td>
<td class="left">Int</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="left">attachmentTimestampLowerBound</td>
<td class="left">Int</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="left">attachmentTimestampUpperBound</td>
<td class="left">Int</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="left">branchTransaction</td>
<td class="left">String</td>
<td class="right">81</td>
</tr>


<tr>
<td class="left">bundle</td>
<td class="left">String</td>
<td class="right">81</td>
</tr>


<tr>
<td class="left">currentIndex</td>
<td class="left">Int</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="left">hash</td>
<td class="left">String</td>
<td class="right">81</td>
</tr>


<tr>
<td class="left">lastIndex</td>
<td class="left">Int</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="left">nonce</td>
<td class="left">String</td>
<td class="right">27</td>
</tr>


<tr>
<td class="left">obsoleteTag</td>
<td class="left">String</td>
<td class="right">27</td>
</tr>


<tr>
<td class="left">signatureMessageFragment</td>
<td class="left">String</td>
<td class="right">2187</td>
</tr>


<tr>
<td class="left">tag</td>
<td class="left">String</td>
<td class="right">27</td>
</tr>


<tr>
<td class="left">timestamp</td>
<td class="left">Int</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="left">trunktransaction</td>
<td class="left">String</td>
<td class="right">81</td>
</tr>


<tr>
<td class="left">value</td>
<td class="left">Int</td>
<td class="right">&#xa0;</td>
</tr>


<tr>
<td class="left">TOTAL</td>
<td class="left">&#xa0;</td>
<td class="right">2673</td>
</tr>
</tbody>
</table>

2673 trytes = 8019 trits

# generate iota seed<a id="sec-4" name="sec-4"></a>

cat /dev/urandom |tr -dc A-Z9|head -c${1:-81}

# address<a id="sec-5" name="sec-5"></a>

is 81 trytes + 9 checksum trytes