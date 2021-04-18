---
title: Константы TF_ES_ (Мсктф. h)
description: Ниже приведены константы, используемые методом ITfContext Рекуестедитсессион.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682038"
---
# <a name="tf_es_-constants"></a><span data-ttu-id="411d4-103">\_ \_ \* Константы TF ES</span><span class="sxs-lookup"><span data-stu-id="411d4-103">TF\_ES\_\* Constants</span></span>

<span data-ttu-id="411d4-104">Ниже приведены константы, используемые методом [ITfContext:: рекуестедитсессион](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .</span><span class="sxs-lookup"><span data-stu-id="411d4-104">The following are constants used by the [ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) method.</span></span>



| <span data-ttu-id="411d4-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="411d4-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="411d4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="411d4-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <span data-ttu-id="411d4-107"><dt>**Tf \_ \_АСИНКДОНТКАРЕ ES**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="411d4-107"><dt>**TF\_ES\_ASYNCDONTCARE**</dt> <dt>( 0 )</dt></span></span> </dl> | <span data-ttu-id="411d4-108">Сеанс изменения может происходить синхронно или асинхронно по собственному усмотрению руководителя.</span><span class="sxs-lookup"><span data-stu-id="411d4-108">The edit session can occur synchronously or asynchronously, at the discretion of the manager.</span></span> <span data-ttu-id="411d4-109">Руководитель попытается запланировать синхронный сеанс редактирования, чтобы повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="411d4-109">The manager will attempt to schedule a synchronous edit session for improved performance.</span></span> <span data-ttu-id="411d4-110">Это значение не может быть объединено со \_ значениями для синхронизации TF ES \_ Async или TF \_ ES \_ .</span><span class="sxs-lookup"><span data-stu-id="411d4-110">This value cannot be combined with the TF\_ES\_ASYNC or TF\_ES\_SYNC values.</span></span><br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <span data-ttu-id="411d4-111"><dt>**Tf \_ \_Синхронизация ES**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="411d4-111"><dt>**TF\_ES\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                          | <span data-ttu-id="411d4-112">Сеанс редактирования должен быть синхронным, иначе запрос завершится ошибкой (с помощью TF \_ E \_ синхронно).</span><span class="sxs-lookup"><span data-stu-id="411d4-112">The edit session must be synchronous or the request will fail (with TF\_E\_SYNCHRONOUS).</span></span> <span data-ttu-id="411d4-113">Этот флаг следует использовать только в документированных ситуациях (например, при обработке нажатий клавиш), где его выполнение может быть ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="411d4-113">This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed.</span></span> <span data-ttu-id="411d4-114">В противном случае вызов, скорее всего, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="411d4-114">Otherwise the call will likely fail.</span></span> <span data-ttu-id="411d4-115">Это значение нельзя сочетать с \_ \_ асинхронными значениями TF ES АСИНКДОНТКАРЕ или TF \_ ES \_ .</span><span class="sxs-lookup"><span data-stu-id="411d4-115">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_ASYNC values.</span></span><br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <span data-ttu-id="411d4-116"><dt>**Tf \_ \_Чтение ES**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="411d4-116"><dt>**TF\_ES\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                          | <span data-ttu-id="411d4-117">Запрашивает доступ только для чтения к контексту.</span><span class="sxs-lookup"><span data-stu-id="411d4-117">Requests read-only access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <span data-ttu-id="411d4-118"><dt>**Tf \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="411d4-118"><dt>**TF\_ES\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl>           | <span data-ttu-id="411d4-119">Запрашивает доступ для чтения и записи к контексту.</span><span class="sxs-lookup"><span data-stu-id="411d4-119">Requests read/write access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <span data-ttu-id="411d4-120"><dt>**Tf \_ ES \_ Async**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="411d4-120"><dt>**TF\_ES\_ASYNC**</dt> <dt>( 0x8 )</dt></span></span> </dl>                       | <span data-ttu-id="411d4-121">Сеанс редактирования должен быть асинхронным, иначе запрос завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="411d4-121">The edit session must be asynchronous or the request will fail.</span></span> <span data-ttu-id="411d4-122">Это значение не может быть объединено со \_ \_ значениями для параметров синхронизации TF ES АСИНКДОНТКАРЕ или TF \_ ES \_ .</span><span class="sxs-lookup"><span data-stu-id="411d4-122">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_SYNC values.</span></span><br/>                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="411d4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="411d4-123">Requirements</span></span>



| <span data-ttu-id="411d4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="411d4-124">Requirement</span></span> | <span data-ttu-id="411d4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="411d4-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="411d4-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="411d4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="411d4-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="411d4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="411d4-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="411d4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="411d4-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="411d4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="411d4-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="411d4-130">Redistributable</span></span><br/>          | <span data-ttu-id="411d4-131">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="411d4-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="411d4-132">Header</span><span class="sxs-lookup"><span data-stu-id="411d4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="411d4-133"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="411d4-133"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="411d4-134">IDL</span><span class="sxs-lookup"><span data-stu-id="411d4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="411d4-135"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="411d4-135"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="411d4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="411d4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="411d4-137">ITfContext:: Рекуестедитсессион</span><span class="sxs-lookup"><span data-stu-id="411d4-137">ITfContext::RequestEditSession</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





