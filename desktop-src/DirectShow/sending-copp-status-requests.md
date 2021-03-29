---
description: Отправка запросов состояния Копп
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Отправка запросов состояния Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805212"
---
# <a name="sending-copp-status-requests"></a><span data-ttu-id="aea0c-103">Отправка запросов состояния Копп</span><span class="sxs-lookup"><span data-stu-id="aea0c-103">Sending COPP Status Requests</span></span>

<span data-ttu-id="aea0c-104">Чтобы отправить запрос о состоянии сертифицированного протокола выходной защиты (Копп), заполните структуру [**амкоппстатусинпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) данными запроса.</span><span class="sxs-lookup"><span data-stu-id="aea0c-104">To send a Certified Output Protection Protocol (COPP) status request, fill in an [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure with the request data.</span></span> <span data-ttu-id="aea0c-105">Члены структуры:</span><span class="sxs-lookup"><span data-stu-id="aea0c-105">The structure members are:</span></span>

-   <span data-ttu-id="aea0c-106">**Рапп**.</span><span class="sxs-lookup"><span data-stu-id="aea0c-106">**rApp**.</span></span> <span data-ttu-id="aea0c-107">128-разрядное случайное число, введенное как идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="aea0c-107">A 128-bit random number, typed as a GUID.</span></span> <span data-ttu-id="aea0c-108">В ответе драйвера возвращается то же число.</span><span class="sxs-lookup"><span data-stu-id="aea0c-108">The same number is returned in the driver's response.</span></span> <span data-ttu-id="aea0c-109">Необходимо выделить случайное число в куче, а затем скопировать его в структуру.</span><span class="sxs-lookup"><span data-stu-id="aea0c-109">You should allocate the random number on the heap and then copy it into structure.</span></span> <span data-ttu-id="aea0c-110">Это защищает от атак, в которых злоумышленник изменяет содержимое структуры [**амкоппстатусинпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .</span><span class="sxs-lookup"><span data-stu-id="aea0c-110">This guards against attacks where the attacker modifies the contents of the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure.</span></span>
-   <span data-ttu-id="aea0c-111">**гуидстатусрекуестид**.</span><span class="sxs-lookup"><span data-stu-id="aea0c-111">**guidStatusRequestID**.</span></span> <span data-ttu-id="aea0c-112">Идентификатор GUID, определяющий запрос.</span><span class="sxs-lookup"><span data-stu-id="aea0c-112">A GUID that identifies the request.</span></span> <span data-ttu-id="aea0c-113">См. [Справочник по запросам Копп](copp-query-reference.md).</span><span class="sxs-lookup"><span data-stu-id="aea0c-113">See [COPP Query Reference](copp-query-reference.md).</span></span>
-   <span data-ttu-id="aea0c-114">**двсекуенце**.</span><span class="sxs-lookup"><span data-stu-id="aea0c-114">**dwSequence**.</span></span> <span data-ttu-id="aea0c-115">Порядковый номер состояния.</span><span class="sxs-lookup"><span data-stu-id="aea0c-115">The status sequence number.</span></span> <span data-ttu-id="aea0c-116">Увеличить это значение после каждого запроса состояния.</span><span class="sxs-lookup"><span data-stu-id="aea0c-116">Increment this value after each status request.</span></span> <span data-ttu-id="aea0c-117">(В разделе, [запускающем сеанс Копп](initiating-a-copp-session.md), это значение отображается как *устатуссек* в примерах кода.)</span><span class="sxs-lookup"><span data-stu-id="aea0c-117">(In the section [Initiating a COPP Session](initiating-a-copp-session.md), this value is shown as *uStatusSeq* in the code examples.)</span></span>
-   <span data-ttu-id="aea0c-118">**кбсизедата**.</span><span class="sxs-lookup"><span data-stu-id="aea0c-118">**cbSizeData**.</span></span> <span data-ttu-id="aea0c-119">Размер (в байтах) дополнительных данных, необходимых для запроса.</span><span class="sxs-lookup"><span data-stu-id="aea0c-119">The size, in bytes, of any additional data needed for the request.</span></span>
-   <span data-ttu-id="aea0c-120">**StatusData**.</span><span class="sxs-lookup"><span data-stu-id="aea0c-120">**StatusData**.</span></span> <span data-ttu-id="aea0c-121">Данные для запроса состояния.</span><span class="sxs-lookup"><span data-stu-id="aea0c-121">Data for the status request.</span></span>

<span data-ttu-id="aea0c-122">Передайте структуру [**амкоппстатусинпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) в метод [**Иамцертифиедаутпутпротектион::P ротектионстатус**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) .</span><span class="sxs-lookup"><span data-stu-id="aea0c-122">Pass the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure to the [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) method.</span></span> <span data-ttu-id="aea0c-123">Например, следующий код отправляет запрос состояния, который запрашивает доступные механизмы защиты:</span><span class="sxs-lookup"><span data-stu-id="aea0c-123">For example, the following code sends a status request that queries which protection mechanisms are available:</span></span>


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



<span data-ttu-id="aea0c-124">Ответ записывается в элемент **коппстатус** структуры [**амкоппстатусаутпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) .</span><span class="sxs-lookup"><span data-stu-id="aea0c-124">The response is written into the **COPPStatus** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure.</span></span> <span data-ttu-id="aea0c-125">Размер допустимых данных в ответе указывается в элементе **кбсизедата** .</span><span class="sxs-lookup"><span data-stu-id="aea0c-125">The size of the valid data in the response is given in the **cbSizeData** member.</span></span> <span data-ttu-id="aea0c-126">Чтобы обеспечить целостность сообщения, драйвер рассчитывает код проверки подлинности сообщения (MAC) с помощью алгоритма ОМАК 1 и возвращает это значение в элемент **маккди** структуры.</span><span class="sxs-lookup"><span data-stu-id="aea0c-126">To ensure the integrity of the message, the driver computes a message authentication code (MAC) using the OMAC 1 algorithm, and returns this value in the structure's **macKDI** member.</span></span> <span data-ttu-id="aea0c-127">Приложение должно проверить это значение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aea0c-127">The application should verify this value as follows:</span></span>

1.  <span data-ttu-id="aea0c-128">Вычислите тег ОМАК для блока данных, который отображается после элемента **маккди** структуры [**амкоппстатусаутпут**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (иными словами, **кбсизедата** и **коппстатус**).</span><span class="sxs-lookup"><span data-stu-id="aea0c-128">Calculate the OMAC tag for the block of data that appears after the **macKDI** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure (in other words, **cbSizeData** plus **COPPStatus**).</span></span>
2.  <span data-ttu-id="aea0c-129">Сравните этот тег со значением в **маккди**, используя прямую **memcmp**.</span><span class="sxs-lookup"><span data-stu-id="aea0c-129">Compare this tag with the value in **macKDI**, using a straight **memcmp**.</span></span>

<span data-ttu-id="aea0c-130">Алгоритм ОМАК 1 подробно описан в разделе [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) .</span><span class="sxs-lookup"><span data-stu-id="aea0c-130">The OMAC 1 algorithm is described in detail at [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html).</span></span> <span data-ttu-id="aea0c-131">Копп использует следующие параметры ОМАК-1:</span><span class="sxs-lookup"><span data-stu-id="aea0c-131">COPP uses the following OMAC-1 parameters:</span></span>

-   <span data-ttu-id="aea0c-132">E = AES</span><span class="sxs-lookup"><span data-stu-id="aea0c-132">E = AES</span></span>
-   <span data-ttu-id="aea0c-133">t = 128 бит</span><span class="sxs-lookup"><span data-stu-id="aea0c-133">t = 128 bits</span></span>

<span data-ttu-id="aea0c-134">Данные, возвращаемые запросом состояния, всегда начинаются с двух элементов:</span><span class="sxs-lookup"><span data-stu-id="aea0c-134">The data returned from the status request always starts with two items:</span></span>

-   <span data-ttu-id="aea0c-135">То же значение **Рапп** , которое было передано приложением.</span><span class="sxs-lookup"><span data-stu-id="aea0c-135">The same value of **rApp** that was passed by the application.</span></span> <span data-ttu-id="aea0c-136">Следует убедиться, что это значение совпадает с исходным значением, хранящимся в куче.</span><span class="sxs-lookup"><span data-stu-id="aea0c-136">You should verify that this value matches the original value stored on the heap.</span></span>
-   <span data-ttu-id="aea0c-137">Значение [**Копп \_ статусфлагс**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) , указывающее, изменилось ли состояние защиты вывода.</span><span class="sxs-lookup"><span data-stu-id="aea0c-137">A [**COPP\_StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) value that indicates whether the output protection status has changed.</span></span>

<span data-ttu-id="aea0c-138">Так как подключение может быть потеряно или перенастроено, приложение должно периодически опрашивать драйвер на предмет текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="aea0c-138">Because the connection can be lost or reconfigured, the application should periodically poll the driver for the current status.</span></span> <span data-ttu-id="aea0c-139">Если установлен \_ флаг Копп ренеготиатионрекуиред, приложение должно попытаться сбросить уровень защиты.</span><span class="sxs-lookup"><span data-stu-id="aea0c-139">If the COPP\_RenegotiationRequired flag is set, the application should attempt to reset the protection level.</span></span> <span data-ttu-id="aea0c-140">Если установлен \_ флаг Копп линклост, приложение должно закончить воспроизведение содержимого.</span><span class="sxs-lookup"><span data-stu-id="aea0c-140">If the COPP\_LinkLost flag is set, the application should stop playing the content.</span></span> <span data-ttu-id="aea0c-141">Например, \_ можно вернуть флаг Копп линклост, так как пользователь отключил выходной соединитель.</span><span class="sxs-lookup"><span data-stu-id="aea0c-141">For example, the COPP\_LinkLost flag can be returned because the user disconnected the output connector.</span></span> <span data-ttu-id="aea0c-142">Приложение должно освободить текущий экземпляр VMR, создать новый экземпляр VMR и установить новый сеанс Копп (включая обмен ключами и проверку сертификата).</span><span class="sxs-lookup"><span data-stu-id="aea0c-142">The application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aea0c-143">См. также</span><span class="sxs-lookup"><span data-stu-id="aea0c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aea0c-144">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="aea0c-144">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



