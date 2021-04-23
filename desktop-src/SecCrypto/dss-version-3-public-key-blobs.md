---
description: Для экспорта и импорта сведений о открытом ключе Диффи-Хелмана используются открытые ключи BLOB-объектов DSS версии 3 типа ПУБЛИККЭЙБЛОБ.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: BLOB-объекты открытого ключа DSS версии 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662309"
---
# <a name="dss-version-3-public-key-blobs"></a><span data-ttu-id="38bbd-103">BLOB-объекты открытого ключа DSS версии 3</span><span class="sxs-lookup"><span data-stu-id="38bbd-103">DSS Version 3 Public Key BLOBs</span></span>

<span data-ttu-id="38bbd-104">Для экспорта и импорта сведений о открытом ключе Диффи-Хелмана используются [*открытые ключи BLOB-объектов*](../secgloss/p-gly.md) DSS версии 3 типа публиккэйблоб.</span><span class="sxs-lookup"><span data-stu-id="38bbd-104">DSS version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) of type PUBLICKEYBLOB are used to export and import information about a DH public key.</span></span> <span data-ttu-id="38bbd-105">Они имеют следующий формат:</span><span class="sxs-lookup"><span data-stu-id="38bbd-105">They have the following format:</span></span>


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



<span data-ttu-id="38bbd-106">Этот формат [*большого двоичного объекта*](../secgloss/b-gly.md) экспортируется, когда \_ флаг шифрования BLOB \_ -объекта VER3 используется с [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="38bbd-106">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="38bbd-107">Так как версия находится в большом двоичном объекте, нет необходимости указывать флаг при использовании этого большого двоичного объекта с [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="38bbd-107">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="38bbd-108">Кроме того, этот формат больших двоичных объектов используется с функцией [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , если параметр *двпарам* значение параметра \_ Pub \_ используется для задания параметров ключа в DSS-ключе.</span><span class="sxs-lookup"><span data-stu-id="38bbd-108">In addition, this BLOB format is used with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function when the *dwParam* value KP\_PUB\_PARAMS is used to set key parameters on a DSS key.</span></span> <span data-ttu-id="38bbd-109">Это делается, если \_ для создания ключа использовался флаг шифрования прежен.</span><span class="sxs-lookup"><span data-stu-id="38bbd-109">This is done when the CRYPT\_PREGEN flag has been used to generate the key.</span></span> <span data-ttu-id="38bbd-110">При использовании в этой ситуации значение y игнорируется и поэтому не должно включаться в большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="38bbd-110">When used in this situation, the y value is ignored and therefore should not be included in the BLOB.</span></span>

<span data-ttu-id="38bbd-111">В следующей таблице описаны все компоненты большого двоичного объекта ключа.</span><span class="sxs-lookup"><span data-stu-id="38bbd-111">The following table describes each component of the key BLOB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38bbd-112">Поле</span><span class="sxs-lookup"><span data-stu-id="38bbd-112">Field</span></span></th>
<th><span data-ttu-id="38bbd-113">Описание</span><span class="sxs-lookup"><span data-stu-id="38bbd-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38bbd-114">блобхеадер</span><span class="sxs-lookup"><span data-stu-id="38bbd-114">Blobheader</span></span></td>
<td><span data-ttu-id="38bbd-115">Структура <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>блобхеадер</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="38bbd-115">A <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> structure.</span></span> <span data-ttu-id="38bbd-116">Элемент <strong>бтипе</strong> должен иметь значение публиккэйблоб.</span><span class="sxs-lookup"><span data-stu-id="38bbd-116">The <strong>bType</strong> member must have a value of PUBLICKEYBLOB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bbd-117">Dsspubkeyver3</span><span class="sxs-lookup"><span data-stu-id="38bbd-117">Dsspubkeyver3</span></span></td>
<td><span data-ttu-id="38bbd-118">Структура <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="38bbd-118">A <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure.</span></span> <span data-ttu-id="38bbd-119">Для открытых ключей необходимо задать для элемента <strong>Magic</strong> значение &quot; DSS3 &quot; (0x33535344).</span><span class="sxs-lookup"><span data-stu-id="38bbd-119">The <strong>magic</strong> member should be set to &quot;DSS3&quot; (0x33535344) for public keys.</span></span> <span data-ttu-id="38bbd-120">Обратите внимание, что шестнадцатеричное значение — это просто кодировка <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> для &quot; DSS3.&quot;</span><span class="sxs-lookup"><span data-stu-id="38bbd-120">Notice that the hexadecimal value is just an <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> encoding of &quot;DSS3.&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bbd-121">С</span><span class="sxs-lookup"><span data-stu-id="38bbd-121">P</span></span></td>
<td><span data-ttu-id="38bbd-122">Значение P размещается непосредственно после структуры <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> и всегда должно быть длиной в байтах поля DSSPUBKEY_VER3 <strong>битленп</strong> (разрядная длина P), разделенного на 8 (формат с<a href="/windows/desktop/SecGloss/l-gly"><em>прямым порядком байтов</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="38bbd-122">The P value is located directly after the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure, and should always be the length, in bytes, of the DSSPUBKEY_VER3 <strong>bitlenP</strong> field (bit length of P) divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bbd-123">Q</span><span class="sxs-lookup"><span data-stu-id="38bbd-123">Q</span></span></td>
<td><span data-ttu-id="38bbd-124">Значение Q находится непосредственно после значения P и всегда должно быть длиной в байтах <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>элемента<strong>битленк</strong> , разделенного на восемь (формат с<a href="/windows/desktop/SecGloss/l-gly"><em>прямым порядком байтов</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="38bbd-124">The Q value is located directly after the P value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bbd-125">G</span><span class="sxs-lookup"><span data-stu-id="38bbd-125">G</span></span></td>
<td><span data-ttu-id="38bbd-126">Значение G расположено непосредственно после значения Q и всегда должно быть длиной в байтах <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>элемента<strong>битленп</strong> (разрядность P), разделенного на восемь.</span><span class="sxs-lookup"><span data-stu-id="38bbd-126">The G value is located directly after the Q value and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="38bbd-127">Если длина данных равна одному или нескольким байтам, меньшим, чем P, деленному на 8, то данные должны быть дополнены требуемыми байтами (нулевыми значениями), чтобы данные были требуемой длины (формат с<a href="/windows/desktop/SecGloss/l-gly"><em>прямым порядком байтов</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="38bbd-127">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bbd-128">J</span><span class="sxs-lookup"><span data-stu-id="38bbd-128">J</span></span></td>
<td><span data-ttu-id="38bbd-129">Значение J расположено непосредственно после значения G и всегда должно быть длиной в байтах <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>элемента<strong>битленж</strong> , разделенного на восемь (формат с<a href="/windows/desktop/SecGloss/l-gly"><em>прямым порядком байтов</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="38bbd-129">The J value is located directly after the G value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span> <span data-ttu-id="38bbd-130">Если значение Битленк равно 0, то это значение отсутствует в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="38bbd-130">If the bitlenQ value is 0, then the value is absent from the BLOB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bbd-131">Да</span><span class="sxs-lookup"><span data-stu-id="38bbd-131">Y</span></span></td>
<td><span data-ttu-id="38bbd-132">Значение Y (G ^ X) mod P находится непосредственно после значения J и всегда должно быть длиной (в байтах) <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>элемента<strong>Битленп</strong> (длина P), деленная на восемь.</span><span class="sxs-lookup"><span data-stu-id="38bbd-132">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="38bbd-133">Если длина данных, полученная в результате вычисления (G ^ X) mod P, равна одному или более байтам, меньшим, чем P, то данные должны быть дополнены требуемыми байтами (нулевыми значениями), чтобы данные были требуемой длины (формат с<a href="/windows/desktop/SecGloss/l-gly"><em>прямым порядком байтов</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="38bbd-133">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="38bbd-134">Если эта структура используется с <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>криптсеткэйпарам</strong></a> со значением <em>двпарам</em> KP_PUB_PARAMS, то это значение не включается в большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="38bbd-134">When this structure is used with <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> with the <em>dwParam</em> value KP_PUB_PARAMS, then this value is not included in the BLOB.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="38bbd-135">Большие двоичные объекты с открытым ключом не шифруются, но содержат открытые ключи в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="38bbd-135">Public key BLOBs are not encrypted, but contain public keys in plaintext form.</span></span>

 

 

 
