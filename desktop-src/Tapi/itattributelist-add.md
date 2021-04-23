---
description: Метод Add добавляет атрибут по указанному индексу.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'Метод Итаттрибутелист:: Add (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680000"
---
# <a name="itattributelistadd-method"></a><span data-ttu-id="34c9f-103">Метод Итаттрибутелист:: Add</span><span class="sxs-lookup"><span data-stu-id="34c9f-103">ITAttributeList::Add method</span></span>

<span data-ttu-id="34c9f-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="34c9f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="34c9f-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="34c9f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="34c9f-106">Метод **Add** добавляет атрибут по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="34c9f-106">The **Add** method adds the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="34c9f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34c9f-107">Syntax</span></span>


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="34c9f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="34c9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34c9f-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34c9f-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34c9f-110">Индекс добавляемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="34c9f-110">Index of the attribute to add.</span></span>

</dd> <dt>

<span data-ttu-id="34c9f-111">*паттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34c9f-111">*pAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34c9f-112">Указатель на **BSTR** , содержащий значение добавляемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="34c9f-112">Pointer to a **BSTR** containing the value of the attribute to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34c9f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34c9f-113">Return value</span></span>

<span data-ttu-id="34c9f-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="34c9f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="34c9f-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="34c9f-115">Return code</span></span>                                                                                   | <span data-ttu-id="34c9f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="34c9f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="34c9f-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="34c9f-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="34c9f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="34c9f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="34c9f-120">Недопустимый параметр *index* или *паттрибуте* .</span><span class="sxs-lookup"><span data-stu-id="34c9f-120">The *Index* or *pAttribute* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="34c9f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="34c9f-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="34c9f-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="34c9f-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="34c9f-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="34c9f-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="34c9f-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="34c9f-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="34c9f-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="34c9f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34c9f-127">Remarks</span></span>

<span data-ttu-id="34c9f-128">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Паттрибуте* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="34c9f-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAttribute* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="34c9f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="34c9f-129">Requirements</span></span>



| <span data-ttu-id="34c9f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="34c9f-130">Requirement</span></span> | <span data-ttu-id="34c9f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="34c9f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34c9f-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="34c9f-132">TAPI version</span></span><br/> | <span data-ttu-id="34c9f-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="34c9f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="34c9f-134">Header</span><span class="sxs-lookup"><span data-stu-id="34c9f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="34c9f-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="34c9f-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34c9f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="34c9f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="34c9f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="34c9f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="34c9f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34c9f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c9f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34c9f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c9f-141">**итаттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="34c9f-141">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

