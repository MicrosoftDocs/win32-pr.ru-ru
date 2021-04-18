---
description: Предоставляет доступ к памяти, используемой между потоками планшета.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'Метод Итаблетконтекстп:: Усешаредмеморикоммуникатионс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713064"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a><span data-ttu-id="e733a-103">Метод Итаблетконтекстп:: Усешаредмеморикоммуникатионс</span><span class="sxs-lookup"><span data-stu-id="e733a-103">ITabletContextP::UseSharedMemoryCommunications method</span></span>

<span data-ttu-id="e733a-104">Предоставляет доступ к памяти, используемой между потоками планшета.</span><span class="sxs-lookup"><span data-stu-id="e733a-104">Provides access to memory shared between tablet threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="e733a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e733a-105">Syntax</span></span>


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a><span data-ttu-id="e733a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e733a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e733a-107">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e733a-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e733a-108">Идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="e733a-108">Process id.</span></span>

</dd> <dt>

<span data-ttu-id="e733a-109">*февентморедата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e733a-109">*phEventMoreData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e733a-110">Обработчик событий, посылает сигнал о том, что новые данные доступны для обработки.</span><span class="sxs-lookup"><span data-stu-id="e733a-110">Event handle that signals when new data is available to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="e733a-111">*февентклиентреади* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e733a-111">*phEventClientReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e733a-112">Возвращенный дескриптор события, используемый для сигнализации о готовности клиента к приему данных.</span><span class="sxs-lookup"><span data-stu-id="e733a-112">Returned event handle used to signal that the client is ready to receive data.</span></span> <span data-ttu-id="e733a-113">Подается сигнал после обработки новых данных.</span><span class="sxs-lookup"><span data-stu-id="e733a-113">Signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="e733a-114">*фмутексакцесс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e733a-114">*phMutexAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e733a-115">Мьютекс, предоставляющий доступ к общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e733a-115">The mutex granting access to shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="e733a-116">*ффилемаппинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e733a-116">*phFileMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e733a-117">Указатель на блок общей памяти.</span><span class="sxs-lookup"><span data-stu-id="e733a-117">Pointer to the shared memory block.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e733a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e733a-118">Return value</span></span>

<span data-ttu-id="e733a-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e733a-119">This method can return one of these values.</span></span>



| <span data-ttu-id="e733a-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e733a-120">Return code</span></span>                                                                            | <span data-ttu-id="e733a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e733a-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e733a-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e733a-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e733a-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e733a-123">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e733a-124"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="e733a-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e733a-125">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e733a-125">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e733a-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e733a-126">Remarks</span></span>

<span data-ttu-id="e733a-127">Метод **усешаредмеморикоммуникатионс** используется как часть протокола общей памяти Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e733a-127">The **UseSharedMemoryCommunications** method is used as part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="e733a-128">Так как служба Висптис имеет высокий уровень целостности (IL), она может хранить и получать доступ к данным, хранящимся в общей памяти, без необходимости повышать свои привилегии.</span><span class="sxs-lookup"><span data-stu-id="e733a-128">Since the Wisptis service has a high integrity level (IL), it can store and access data stored in shared memory without needing to elevate its privileges.</span></span>

<span data-ttu-id="e733a-129">Структура [**\_ заголовка шаредмемори**](sharedmemory-header.md) приводится к данным, на которые ссылается сопоставление файлов, а необработанные данные пакетов следуют **\_ заголовку шаредмемори**.</span><span class="sxs-lookup"><span data-stu-id="e733a-129">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping and the raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="e733a-130">Необработанные данные пакетов можно считывать из общей памяти при возникновении события, на которое ссылается *пдвевентклиентреади* .</span><span class="sxs-lookup"><span data-stu-id="e733a-130">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReady* is raised.</span></span>

<span data-ttu-id="e733a-131">В следующем списке приводится последовательность событий для доступа к общей памяти и использования ее.</span><span class="sxs-lookup"><span data-stu-id="e733a-131">The following list describes the sequence of events for accessing and using shared memory.</span></span>

-   <span data-ttu-id="e733a-132">Клиент устанавливает событие Клиентреади.</span><span class="sxs-lookup"><span data-stu-id="e733a-132">The client sets the clientReady event.</span></span>
-   <span data-ttu-id="e733a-133">Клиент ожидает события moreData.</span><span class="sxs-lookup"><span data-stu-id="e733a-133">The client waits for the moreData event.</span></span>
-   <span data-ttu-id="e733a-134">Клиент получает мьютекс.</span><span class="sxs-lookup"><span data-stu-id="e733a-134">The client acquires the mutex.</span></span>
-   <span data-ttu-id="e733a-135">Клиент считывает данные пакета из раздела общей памяти после заголовков и серийных номеров после пакетов.</span><span class="sxs-lookup"><span data-stu-id="e733a-135">The client reads packet data from the section of shared memory after the header and serial numbers after the packets.</span></span>
-   <span data-ttu-id="e733a-136">Клиент обрабатывает данные в зависимости от значения **двевент**.</span><span class="sxs-lookup"><span data-stu-id="e733a-136">The client handles data depending on the value of **dwEvent**.</span></span>
-   <span data-ttu-id="e733a-137">Клиент записывает-1 (0xFFFFFFFF) в **двевент**.</span><span class="sxs-lookup"><span data-stu-id="e733a-137">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
-   <span data-ttu-id="e733a-138">Клиент освобождает мьютекс.</span><span class="sxs-lookup"><span data-stu-id="e733a-138">The client releases the mutex.</span></span>
-   <span data-ttu-id="e733a-139">Клиент устанавливает событие Клиентреади.</span><span class="sxs-lookup"><span data-stu-id="e733a-139">The client sets the clientReady event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e733a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="e733a-140">Requirements</span></span>



| <span data-ttu-id="e733a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="e733a-141">Requirement</span></span> | <span data-ttu-id="e733a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="e733a-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e733a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e733a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e733a-144">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e733a-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e733a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e733a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e733a-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e733a-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e733a-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e733a-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="e733a-148"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e733a-148"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e733a-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e733a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e733a-150">**Интерфейс Итаблетконтекстп**</span><span class="sxs-lookup"><span data-stu-id="e733a-150">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="e733a-151">**усенамедшаредмеморикоммуникатионс**</span><span class="sxs-lookup"><span data-stu-id="e733a-151">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




