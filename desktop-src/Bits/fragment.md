---
title: Fragment
description: Используйте пакет фрагмента, чтобы отправить фрагмент файла отправки на сервер.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- БИТЫ фрагмента
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104133515"
---
# <a name="fragment"></a><span data-ttu-id="486cb-104">Fragment</span><span class="sxs-lookup"><span data-stu-id="486cb-104">Fragment</span></span>

<span data-ttu-id="486cb-105">Используйте пакет **фрагмента** , чтобы отправить фрагмент файла отправки на сервер.</span><span class="sxs-lookup"><span data-stu-id="486cb-105">Use the **Fragment** packet to send a fragment of the upload file to the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a><span data-ttu-id="486cb-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="486cb-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="486cb-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS</span><span class="sxs-lookup"><span data-stu-id="486cb-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="486cb-108">Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.</span><span class="sxs-lookup"><span data-stu-id="486cb-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="486cb-109">Замените Remote-URL абсолютным или относительным URI.</span><span class="sxs-lookup"><span data-stu-id="486cb-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="486cb-110">Обычно замените Remote-URL именем удаленного файла задания.</span><span class="sxs-lookup"><span data-stu-id="486cb-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="486cb-111">Рекомендации по балансировке сетевой нагрузки см. в заголовке BITS-Host-ID в пакете [**создания сеанса**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="486cb-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="486cb-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="486cb-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="486cb-113">Идентифицирует этот пакет запроса как пакет фрагмента.</span><span class="sxs-lookup"><span data-stu-id="486cb-113">Identifies this request packet as a Fragment packet.</span></span>

</dd> <dt>

<span data-ttu-id="486cb-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID</span><span class="sxs-lookup"><span data-stu-id="486cb-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="486cb-115">Строковый идентификатор GUID, определяющий сеанс на сервере.</span><span class="sxs-lookup"><span data-stu-id="486cb-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="486cb-116">Замените {GUID} идентификатором сеанса, возвращаемым сервером в ответ на запрос на создание пакета ответа [**для создания сеанса**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="486cb-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> <dt>

<span data-ttu-id="486cb-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span><span class="sxs-lookup"><span data-stu-id="486cb-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span></span>
</dt> <dd>

<span data-ttu-id="486cb-118">Укажите этот заголовок только с начальным фрагментом.</span><span class="sxs-lookup"><span data-stu-id="486cb-118">Specify this header only with the initial fragment.</span></span> <span data-ttu-id="486cb-119">Замените filename именем локального файла в задании.</span><span class="sxs-lookup"><span data-stu-id="486cb-119">Replace filename with the name of the local file name from the job.</span></span> <span data-ttu-id="486cb-120">Имя не включает путь.</span><span class="sxs-lookup"><span data-stu-id="486cb-120">The name does not include the path.</span></span>

</dd> <dt>

<span data-ttu-id="486cb-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого</span><span class="sxs-lookup"><span data-stu-id="486cb-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="486cb-122">Замените length числом байтов, отправленных в тексте фрагмента.</span><span class="sxs-lookup"><span data-stu-id="486cb-122">Replace length with the number of bytes sent in the fragment body.</span></span>

</dd> <dt>

<span data-ttu-id="486cb-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Диапазон содержимого</span><span class="sxs-lookup"><span data-stu-id="486cb-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="486cb-124">Указывает серверу, куда применять диапазон в целевом файле.</span><span class="sxs-lookup"><span data-stu-id="486cb-124">Tells the server where to apply the range in the destination file.</span></span> <span data-ttu-id="486cb-125">Замените Range на начальное и конечное смещение диапазона в целевом файле.</span><span class="sxs-lookup"><span data-stu-id="486cb-125">Replace range with the start and end offsets of the range in the destination file.</span></span> <span data-ttu-id="486cb-126">Смещение отсчитывается от нуля.</span><span class="sxs-lookup"><span data-stu-id="486cb-126">The offsets are zero-based.</span></span> <span data-ttu-id="486cb-127">Если заданный диапазон перекрывает существующий диапазон, BITS записывает только неперекрывающиеся части диапазона; BITS не перезаписывает существующее содержимое.</span><span class="sxs-lookup"><span data-stu-id="486cb-127">If the given range overlaps an existing range, BITS writes only the non-overlapping portion of the range; BITS does not overwrite existing content.</span></span> <span data-ttu-id="486cb-128">Например, если первый пакет содержал диапазон от 0 до 100, а второй пакет содержал диапазон от 50 до 150, BITS записывает только байты с 101 по 150 из второго пакета.</span><span class="sxs-lookup"><span data-stu-id="486cb-128">For example, if the first packet contained the range 0 through 100 and the second packet contained the range 50 through 150, BITS writes only bytes 101 through 150 from the second packet.</span></span> <span data-ttu-id="486cb-129">Замените Total — length общим числом байтов в файле.</span><span class="sxs-lookup"><span data-stu-id="486cb-129">Replace total-length with the total number of bytes in the file.</span></span>

</dd> <dt>

<span data-ttu-id="486cb-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Кодирование содержимого</span><span class="sxs-lookup"><span data-stu-id="486cb-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="486cb-131">Замените кодировку типом кодировки, используемой клиентом в фрагменте.</span><span class="sxs-lookup"><span data-stu-id="486cb-131">Replace encoding with the type of encoding the client uses on the fragment.</span></span> <span data-ttu-id="486cb-132">Клиент должен использовать кодировку, которую сервер определяет в заголовке Accept-Encoding [**подтверждения для пакета ответа на создание сеанса**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="486cb-132">The client must use the encoding that the server identifies in the Accept-Encoding header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="486cb-133">Сервер использует тип кодировки для декодирования фрагмента.</span><span class="sxs-lookup"><span data-stu-id="486cb-133">The server uses the encoding type to decode the fragment.</span></span> <span data-ttu-id="486cb-134">Все фрагменты должны указывать одинаковую кодировку.</span><span class="sxs-lookup"><span data-stu-id="486cb-134">All fragments must specify the same encoding.</span></span>

<span data-ttu-id="486cb-135">Не отправляйте этот заголовок, если тип кодировки — Identity.</span><span class="sxs-lookup"><span data-stu-id="486cb-135">Do not send this header if the encoding type is Identity.</span></span> <span data-ttu-id="486cb-136">Сервер BITS поддерживает только кодирование удостоверений.</span><span class="sxs-lookup"><span data-stu-id="486cb-136">The BITS server supports only Identity encoding.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="486cb-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="486cb-137">Remarks</span></span>

<span data-ttu-id="486cb-138">Фрагмент — это диапазон байтов, отправленных в тексте пакета.</span><span class="sxs-lookup"><span data-stu-id="486cb-138">The fragment is a range of bytes sent in the body of the packet.</span></span> <span data-ttu-id="486cb-139">Клиент отправляет фрагменты в последовательном порядке, начиная с нулевого смещения. сервер не отслеживает несмежные диапазоны.</span><span class="sxs-lookup"><span data-stu-id="486cb-139">The client sends the fragments in sequential order starting with offset zero; the server does not keep track of non-contiguous ranges.</span></span> <span data-ttu-id="486cb-140">Если клиент отправляет несмежные диапазоны, сервер возвращает код возврата HTTP 416 (с диапазоном, который не соответствует) в ответе [**ACK для ответа фрагмента**](ack-for-fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="486cb-140">If the client sends non-contiguous ranges, the server returns an HTTP 416 (range-not-satisfiable) return code in the [**Ack for Fragment**](ack-for-fragment.md) response.</span></span>

<span data-ttu-id="486cb-141">Заголовки Content-*XXXX* — это стандартные заголовки HTTP 1,1.</span><span class="sxs-lookup"><span data-stu-id="486cb-141">The Content-*xxxx* headers are standard HTTP 1.1 headers.</span></span> <span data-ttu-id="486cb-142">Дополнительные сведения о заголовках Content-*XXXX* см. в спецификации [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .</span><span class="sxs-lookup"><span data-stu-id="486cb-142">For more details on the Content-*xxxx* headers, see the [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="486cb-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="486cb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="486cb-144">**Подтверждение для фрагмента**</span><span class="sxs-lookup"><span data-stu-id="486cb-144">**Ack for Fragment**</span></span>](ack-for-fragment.md)
</dt> <dt>

[<span data-ttu-id="486cb-145">**Закрыть — сеанс**</span><span class="sxs-lookup"><span data-stu-id="486cb-145">**Close-Session**</span></span>](close-session.md)
</dt> <dt>

[<span data-ttu-id="486cb-146">**Создание сеанса**</span><span class="sxs-lookup"><span data-stu-id="486cb-146">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




