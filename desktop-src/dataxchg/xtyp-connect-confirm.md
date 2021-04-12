---
title: XTYP_CONNECT_CONFIRMная транзакция (Ддемл. h)
description: Функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает \_ \_ транзакцию кстип Connect Confirm, чтобы подтвердить, что диалог был установлен с клиентом, и предоставить серверу этот обработчик диалога.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415653"
---
# <a name="xtyp_connect_confirm-transaction"></a><span data-ttu-id="ae5d1-104">КСТИП \_ подключение \_ подтвердить транзакцию</span><span class="sxs-lookup"><span data-stu-id="ae5d1-104">XTYP\_CONNECT\_CONFIRM transaction</span></span>

<span data-ttu-id="ae5d1-105">Функция обратного вызова сервера платформа динамических данных Exchange (DDE) Получает транзакцию **кстип \_ Connect \_ Confirm** [*, чтобы*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)подтвердить, что диалог был установлен с клиентом, и предоставить серверу этот обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-105">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_CONNECT\_CONFIRM** transaction to confirm that a conversation has been established with a client and to provide the server with the conversation handle.</span></span> <span data-ttu-id="ae5d1-106">Система отправляет эту транзакцию в результате предыдущей транзакции [**кстип \_ Connect**](xtyp-connect.md) или [**кстип \_ вилдконнект**](xtyp-wildconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="ae5d1-106">The system sends this transaction as a result of a previous [**XTYP\_CONNECT**](xtyp-connect.md) or [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="ae5d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae5d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae5d1-108">*утипе*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-109">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="ae5d1-110">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae5d1-112">*хконв*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-113">Маркер нового диалога.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-113">A handle to the new conversation.</span></span>

</dd> <dt>

<span data-ttu-id="ae5d1-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-115">Маркер имени раздела, в котором было установлено диалоговое обсуждение.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-115">A handle to the topic name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="ae5d1-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-117">Маркер имени службы, для которого было установлено диалоговое обсуждение.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-117">A handle to the service name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="ae5d1-118">*хдата*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae5d1-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-121">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae5d1-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="ae5d1-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5d1-123">Указывает, является ли клиент тем же экземпляром приложения, что и сервер.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-123">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="ae5d1-124">Если параметр равен 1, то клиент является тем же экземпляром.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-124">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="ae5d1-125">Если параметр равен 0, то клиент является другим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-125">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae5d1-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae5d1-126">Remarks</span></span>

<span data-ttu-id="ae5d1-127">Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Skip \_ Connect \_** для функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="ae5d1-127">This transaction is filtered if the server application specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="ae5d1-128">Сервер не может заблокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ae5d1-128">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae5d1-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ae5d1-129">Requirements</span></span>



| <span data-ttu-id="ae5d1-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ae5d1-130">Requirement</span></span> | <span data-ttu-id="ae5d1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ae5d1-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5d1-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae5d1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5d1-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ae5d1-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ae5d1-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae5d1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5d1-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ae5d1-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ae5d1-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ae5d1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae5d1-137"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae5d1-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae5d1-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae5d1-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae5d1-139">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ae5d1-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ae5d1-140">**ддеконнект**</span><span class="sxs-lookup"><span data-stu-id="ae5d1-140">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="ae5d1-141">**ддеконнектлист**</span><span class="sxs-lookup"><span data-stu-id="ae5d1-141">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[<span data-ttu-id="ae5d1-142">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="ae5d1-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="ae5d1-143">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ae5d1-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ae5d1-144">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="ae5d1-144">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

