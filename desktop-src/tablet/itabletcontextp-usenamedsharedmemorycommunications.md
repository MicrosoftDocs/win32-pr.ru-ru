---
description: Настраивает обмен данными с общей памятью для контекста планшета.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'Метод Итаблетконтекстп:: Усенамедшаредмеморикоммуникатионс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712207"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a><span data-ttu-id="3e1f8-103">Метод Итаблетконтекстп:: Усенамедшаредмеморикоммуникатионс</span><span class="sxs-lookup"><span data-stu-id="3e1f8-103">ITabletContextP::UseNamedSharedMemoryCommunications method</span></span>

<span data-ttu-id="3e1f8-104">Настраивает обмен данными с общей памятью для контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-104">Sets up shared memory communication for the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e1f8-105">Syntax</span></span>


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a><span data-ttu-id="3e1f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e1f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e1f8-107">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f8-108">Идентификатор процесса клиента, обращающегося к общей памяти.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-108">The process ID of the client that accesses shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f8-109">*псзкаллерсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-109">*pszCallerSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f8-110">Идентификатор безопасности вызывающего объекта функции.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-110">The security identifier of the function caller.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f8-111">*псзкаллеринтегритисид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-111">*pszCallerIntegritySid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f8-112">Идентификатор безопасности, который может проверять целостность вызывающей функции.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-112">The security identifier that can verify the integrity of the calling function.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f8-113">*пдвевентморедатаид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-113">*pdwEventMoreDataId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f8-114">Целое число, используемое для создания имени события.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-114">An integer used to construct the name of an event.</span></span> <span data-ttu-id="3e1f8-115">Событие указывает, есть ли дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-115">The event indicates whether there is more data.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f8-116">*пдвевентклиентреадид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-116">*pdwEventClientReadyId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f8-117">Целое число, используемое для создания имени события.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-117">An integer used to construct the name of an event.</span></span> <span data-ttu-id="3e1f8-118">Событие сигнализирует, что клиент готов к приему данных.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-118">The event signals that the client is ready to receive data.</span></span> <span data-ttu-id="3e1f8-119">Событие сообщается после обработки новых данных.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-119">The event is signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f8-120">*пдвмутексакцессид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-120">*pdwMutexAccessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f8-121">Указатель на идентификатор доступа общей памяти.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-121">A pointer to the access identifier of the shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e1f8-122">*пдвфилемаппингид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-122">*pdwFileMappingId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f8-123">Целое число, определяющее общую память.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-123">An integer that identifies the shared memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e1f8-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e1f8-124">Return value</span></span>

<span data-ttu-id="3e1f8-125">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e1f8-126">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e1f8-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e1f8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e1f8-127">Remarks</span></span>

<span data-ttu-id="3e1f8-128">Метод **усенамедшаредмеморикоммуникатионс** является частью протокола общей памяти Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-128">The **UseNamedSharedMemoryCommunications** method is part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="3e1f8-129">Клиент без повышенных привилегий передает идентификатор безопасности (SID) и идентификатор безопасности уровня целостности (IL-SID), чтобы служба планшета могла использовать списки управления доступом (ACL) для доступа к объектам общей памяти.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-129">A client without elevated privileges passes in a security identifier (SID) and an integrity level security identifier (IL-SID) so that the Tablet service can use access control lists (ACL) to access the shared memory objects.</span></span> <span data-ttu-id="3e1f8-130">Если клиент имеет повышенные привилегии, он должен использовать Усешаредмеморикоммуникатионс — API, который вызывается, если у службы уже есть привилегия с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-130">If the client has elevated privileges, it should use UseSharedMemoryCommunications, which is the API that is called if the service already has an elevated privilege.</span></span>

<span data-ttu-id="3e1f8-131">В [**структуре \_ заголовка шаредмемори**](sharedmemory-header.md) хранится заголовок общей памяти.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-131">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure stores the shared memory header.</span></span>

<span data-ttu-id="3e1f8-132">Структура [**\_ заголовка шаредмемори**](sharedmemory-header.md) приводится к данным, на которые ссылается сопоставление файлов.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-132">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping.</span></span> <span data-ttu-id="3e1f8-133">Необработанные данные пакета следуют **\_ заголовку шаредмемори**.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-133">The raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="3e1f8-134">Необработанные данные пакетов можно считывать из общей памяти при возникновении события, на которое ссылается *пдвевентклиентреадид* .</span><span class="sxs-lookup"><span data-stu-id="3e1f8-134">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReadyId* is raised.</span></span>

<span data-ttu-id="3e1f8-135">В следующем списке приводится последовательность событий для доступа к общей памяти и использования ее.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-135">The following list describes the sequence of events for accessing and using shared memory.</span></span>

1.  <span data-ttu-id="3e1f8-136">Клиент вызывает событие Клиентреади.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-136">The client raises the clientReady event.</span></span>
2.  <span data-ttu-id="3e1f8-137">Клиент ожидает события moreData.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-137">The client waits for the moreData event.</span></span>
3.  <span data-ttu-id="3e1f8-138">Клиент получает мьютекс.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-138">The client acquires the mutex.</span></span>
4.  <span data-ttu-id="3e1f8-139">Клиент считывает данные пакета из раздела общей памяти, который следует за заголовком.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-139">The client reads packet data from the section of shared memory that follows the header.</span></span> <span data-ttu-id="3e1f8-140">Серийные номера отображаются в общей памяти после данных пакета.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-140">Serial numbers appear in the shared memory after the packet data.</span></span>
5.  <span data-ttu-id="3e1f8-141">Клиент обрабатывает данные в зависимости от значения **двевент**.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-141">The client handles data depending on the value of **dwEvent**.</span></span>
6.  <span data-ttu-id="3e1f8-142">Клиент записывает-1 (0xFFFFFFFF) в **двевент**.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-142">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
7.  <span data-ttu-id="3e1f8-143">Клиент освобождает мьютекс.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-143">The client releases the mutex.</span></span>
8.  <span data-ttu-id="3e1f8-144">Клиент вызывает событие Клиентреади.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-144">The client raises the clientReady event.</span></span>

<span data-ttu-id="3e1f8-145">Имена событий создаются путем форматирования выходных данных этого метода.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-145">The event names are created by formatting the output of this method.</span></span> <span data-ttu-id="3e1f8-146">Следующие определения можно использовать в сочетании с sprintf или его эквивалентом для создания имен событий.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-146">The following definitions can be used in conjunction with sprintf or its equivalent to create the event names.</span></span>


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



<span data-ttu-id="3e1f8-147">В каждом определении раздел% d заменяется ИДЕНТИФИКАТОРом процесса, а раздел% u заменяется целым числом, возвращенным в *пдвевентморедатаид* или *пдвевентклиентреадид*.</span><span class="sxs-lookup"><span data-stu-id="3e1f8-147">In each definition, the %d section is replaced with the process ID, and the %u section is replaced with the integer returned in *pdwEventMoreDataId* or *pdwEventClientReadyId*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e1f8-148">Требования</span><span class="sxs-lookup"><span data-stu-id="3e1f8-148">Requirements</span></span>



| <span data-ttu-id="3e1f8-149">Требование</span><span class="sxs-lookup"><span data-stu-id="3e1f8-149">Requirement</span></span> | <span data-ttu-id="3e1f8-150">Значение</span><span class="sxs-lookup"><span data-stu-id="3e1f8-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1f8-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e1f8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3e1f8-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e1f8-152">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3e1f8-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e1f8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3e1f8-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3e1f8-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3e1f8-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e1f8-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e1f8-156"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e1f8-156"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e1f8-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e1f8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e1f8-158">**усешаредмеморикоммуникатионс**</span><span class="sxs-lookup"><span data-stu-id="3e1f8-158">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[<span data-ttu-id="3e1f8-159">**итаблетконтекстп**</span><span class="sxs-lookup"><span data-stu-id="3e1f8-159">**ITabletContextP**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




