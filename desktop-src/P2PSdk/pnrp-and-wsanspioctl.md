---
description: Протокол PNRP использует функцию Всанспиоктл для получения уведомлений об изменениях следующего.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP и Всанспиоктл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663296"
---
# <a name="pnrp-and-wsanspioctl"></a><span data-ttu-id="630f1-103">PNRP и Всанспиоктл</span><span class="sxs-lookup"><span data-stu-id="630f1-103">PNRP and WSANSPIoctl</span></span>

<span data-ttu-id="630f1-104">PNRP использует функцию [**всанспиоктл**](winsock-nsp-reference-links.md) для получения уведомлений об изменениях следующих:</span><span class="sxs-lookup"><span data-stu-id="630f1-104">PNRP uses the [**WSANSPIoctl**](winsock-nsp-reference-links.md) function to receive notifications about changes to the following:</span></span>

-   <span data-ttu-id="630f1-105">Список сетевых облаков</span><span class="sxs-lookup"><span data-stu-id="630f1-105">A network cloud list</span></span>
-   <span data-ttu-id="630f1-106">Доступность результатов запроса разрешения имен</span><span class="sxs-lookup"><span data-stu-id="630f1-106">Availability of results of a name resolution request</span></span>

<span data-ttu-id="630f1-107">Первый вызов [**всалукупсервицебегин**](winsock-nsp-reference-links.md) определяет тип информации, о которой уведомляется клиент.</span><span class="sxs-lookup"><span data-stu-id="630f1-107">The first call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) defines the type of information that a client is notified about.</span></span> <span data-ttu-id="630f1-108">Клиент может получать уведомления с помощью сообщения Windows, подпрограммы завершения, обработчика для объекта ВСАЕВЕНТ или порта.</span><span class="sxs-lookup"><span data-stu-id="630f1-108">A client can be notified with a Windows message, a completion routine, a handle to a WSAEVENT object, or a port.</span></span> <span data-ttu-id="630f1-109">Дополнительные сведения о параметрах и настройке параметра *лпкомплетион* см. в разделе **всанспиоктл**.</span><span class="sxs-lookup"><span data-stu-id="630f1-109">For more information about options and setting the *lpCompletion* parameter, see **WSANSPIoctl**.</span></span>

<span data-ttu-id="630f1-110">Чтобы продолжить получать уведомления после вызова [**всалукупсервиценекст**](winsock-nsp-reference-links.md), приложение должно вызвать **всанспиоктл** еще раз.</span><span class="sxs-lookup"><span data-stu-id="630f1-110">To continue receiving notifications after a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md), an application must call **WSANSPIoctl** again.</span></span>

<span data-ttu-id="630f1-111">Функция [**всалукупсервиценекст**](winsock-nsp-reference-links.md) блокируется, даже если вызывается **всанспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="630f1-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="630f1-112">Перед вызовом **всалукупсервиценекст** приложение должно подождать, пока оно не получит уведомление, если блокировка является проблемой.</span><span class="sxs-lookup"><span data-stu-id="630f1-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

<span data-ttu-id="630f1-113">При вызове этой функции параметры должны иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="630f1-113">When calling this function, the parameters must have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="630f1-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*Функции*</span><span class="sxs-lookup"><span data-stu-id="630f1-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-115">Указывает маркер, возвращаемый [**всалукупсервицебегин**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="630f1-115">Specifies the handle that [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) returns.</span></span>

</dd> <dt>

<span data-ttu-id="630f1-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*двконтролкоде*</span><span class="sxs-lookup"><span data-stu-id="630f1-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-117">Должен быть **\_ NSP \_ уведомления о \_ смене SIO**.</span><span class="sxs-lookup"><span data-stu-id="630f1-117">Must be **SIO\_NSP\_NOTIFY\_CHANGE**.</span></span>

</dd> <dt>

<span data-ttu-id="630f1-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*лпвинбуффер*</span><span class="sxs-lookup"><span data-stu-id="630f1-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-119">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="630f1-119">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="630f1-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*кбинбуффер*</span><span class="sxs-lookup"><span data-stu-id="630f1-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-121">Должен быть равен нулю (0).</span><span class="sxs-lookup"><span data-stu-id="630f1-121">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="630f1-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*лпваутбуффер*</span><span class="sxs-lookup"><span data-stu-id="630f1-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-123">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="630f1-123">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="630f1-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*кбаутбуффер*</span><span class="sxs-lookup"><span data-stu-id="630f1-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-125">Должен быть равен нулю (0).</span><span class="sxs-lookup"><span data-stu-id="630f1-125">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="630f1-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*лпкббитесретурнед*</span><span class="sxs-lookup"><span data-stu-id="630f1-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-127">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="630f1-127">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="630f1-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*лпкомплетион*</span><span class="sxs-lookup"><span data-stu-id="630f1-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span></span>
</dt> <dd>

<span data-ttu-id="630f1-129">Указывает либо **значение NULL** , либо указатель на структуру [**всакомплетион**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="630f1-129">Specifies either **NULL** or a pointer to a [**WSACOMPLETION**](winsock-nsp-reference-links.md) structure.</span></span>

</dd> </dl>

<span data-ttu-id="630f1-130">После получения уведомления вызовите [**всалукупсервиценекст**](winsock-nsp-reference-links.md) один раз, чтобы получить результаты.</span><span class="sxs-lookup"><span data-stu-id="630f1-130">After a notification is received, call [**WSALookupServiceNext**](winsock-nsp-reference-links.md) one time to obtain the results.</span></span>

<span data-ttu-id="630f1-131">Чтобы завершить поиск, вызовите [**всалукупсервицеенд**](winsock-nsp-reference-links.md).</span><span class="sxs-lookup"><span data-stu-id="630f1-131">To end a search, call [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span></span>

## <a name="resolution-notifications"></a><span data-ttu-id="630f1-132">Уведомления о разрешении</span><span class="sxs-lookup"><span data-stu-id="630f1-132">Resolution Notifications</span></span>

<span data-ttu-id="630f1-133">Клиент может получать уведомления каждый раз, когда добавляется запись разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="630f1-133">A client can be notified any time that a name resolution entry is added.</span></span> <span data-ttu-id="630f1-134">Затем клиент вызывает [**всалукупсервиценекст**](winsock-nsp-reference-links.md) для получения данных о разрешении.</span><span class="sxs-lookup"><span data-stu-id="630f1-134">The client then calls [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to obtain the resolution data.</span></span>

<span data-ttu-id="630f1-135">Если клиент не использует этот метод, вызов [**всалукупсервиценекст**](winsock-nsp-reference-links.md) можно заблокировать до наступления указанного времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="630f1-135">If the client does not use this technique, a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) can be blocked until the specified timeout occurs.</span></span>

## <a name="cloud-list-notifications"></a><span data-ttu-id="630f1-136">Уведомления в облачном списке</span><span class="sxs-lookup"><span data-stu-id="630f1-136">Cloud List Notifications</span></span>

<span data-ttu-id="630f1-137">Клиент может получать уведомления каждый раз, когда имеется изменение в наборе облаков.</span><span class="sxs-lookup"><span data-stu-id="630f1-137">A client can be notified any time there is a change to a set of clouds.</span></span>

<span data-ttu-id="630f1-138">Функция [**всалукупсервиценекст**](winsock-nsp-reference-links.md) возвращает **WSA \_ E \_ \_** в качестве разделителя множеств.</span><span class="sxs-lookup"><span data-stu-id="630f1-138">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns **WSA\_E\_NO\_MORE** as a set delimiter.</span></span> <span data-ttu-id="630f1-139">Клиентское приложение должно перечислить существующие облака до тех пор, пока не будет возвращено это сообщение, а затем использовать схему уведомлений для получения последующих изменений по мере их появления.</span><span class="sxs-lookup"><span data-stu-id="630f1-139">The client application must enumerate existing clouds until this message is returned, and then use a notification scheme to retrieve subsequent changes as they occur.</span></span> <span data-ttu-id="630f1-140">Клиентское приложение также может вызывать **всалукупсервиценекст**, но вызов блокируется до тех пор, пока не произойдет изменение.</span><span class="sxs-lookup"><span data-stu-id="630f1-140">A client application can also call **WSALookupServiceNext**, but the call is blocked until a change occurs.</span></span>

<span data-ttu-id="630f1-141">Функция [**всалукупсервиценекст**](winsock-nsp-reference-links.md) возвращает облако в структуре **всакуерисет** .</span><span class="sxs-lookup"><span data-stu-id="630f1-141">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns a cloud in a **WSAQUERYSET** structure.</span></span> <span data-ttu-id="630f1-142">В элементе **дваутпутфлагс** возвращается один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="630f1-142">One of the following flags is returned in the **dwOutputFlags** member.</span></span>



| <span data-ttu-id="630f1-143">Значение</span><span class="sxs-lookup"><span data-stu-id="630f1-143">Value</span></span>               | <span data-ttu-id="630f1-144">Описание</span><span class="sxs-lookup"><span data-stu-id="630f1-144">Description</span></span>                                             |
|---------------------|---------------------------------------------------------|
| <span data-ttu-id="630f1-145">Результат \_ \_ добавлен</span><span class="sxs-lookup"><span data-stu-id="630f1-145">RESULT\_IS\_ADDED</span></span>   | <span data-ttu-id="630f1-146">Добавляется возвращаемое облако.</span><span class="sxs-lookup"><span data-stu-id="630f1-146">The cloud that is returned is added.</span></span>                    |
| <span data-ttu-id="630f1-147">Результат \_ \_ изменен</span><span class="sxs-lookup"><span data-stu-id="630f1-147">RESULT\_IS\_CHANGED</span></span> | <span data-ttu-id="630f1-148">Возвращаемое облако изменилось.</span><span class="sxs-lookup"><span data-stu-id="630f1-148">The cloud that is returned is changed.</span></span>                  |
| <span data-ttu-id="630f1-149">Результат \_ \_ удален</span><span class="sxs-lookup"><span data-stu-id="630f1-149">RESULT\_IS\_DELETED</span></span> | <span data-ttu-id="630f1-150">Возвращенное облако удалено и является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="630f1-150">The cloud that is returned is deleted and is not valid.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="630f1-151">См. также</span><span class="sxs-lookup"><span data-stu-id="630f1-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="630f1-152">PNRP и Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="630f1-152">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="630f1-153">PNRP и Всалукупсервицеенд</span><span class="sxs-lookup"><span data-stu-id="630f1-153">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="630f1-154">PNRP и ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="630f1-154">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="630f1-155">Коды ошибок PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="630f1-155">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="630f1-156">**всанспиоктл**</span><span class="sxs-lookup"><span data-stu-id="630f1-156">**WSANSPIoctl**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="630f1-157">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="630f1-157">**WSALookupServiceBegin**</span></span>
</dt> <dt>

<span data-ttu-id="630f1-158">**всалукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="630f1-158">**WSALookupServiceEnd**</span></span>
</dt> <dt>

<span data-ttu-id="630f1-159">**всакуерисет**</span><span class="sxs-lookup"><span data-stu-id="630f1-159">**WSAQUERYSET**</span></span>
</dt> </dl>

 

 



