---
description: Метод Get \_ Item возвращает атрибут, указанный в индексе.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'Метод Итаттрибутелист:: get_Item (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689348"
---
# <a name="itattributelistget_item-method"></a><span data-ttu-id="831f7-103">Метод Итаттрибутелист:: Get \_ Item</span><span class="sxs-lookup"><span data-stu-id="831f7-103">ITAttributeList::get\_Item method</span></span>

<span data-ttu-id="831f7-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="831f7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="831f7-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="831f7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="831f7-106">Метод **Get \_ Item** возвращает атрибут, указанный в индексе.</span><span class="sxs-lookup"><span data-stu-id="831f7-106">The **get\_Item** method returns the attribute specified by the index.</span></span>

## <a name="syntax"></a><span data-ttu-id="831f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="831f7-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="831f7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="831f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="831f7-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="831f7-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831f7-110">Индекс получаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="831f7-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="831f7-111">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="831f7-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="831f7-112">Указатель на **строку BSTR** , содержащую значения элемента.</span><span class="sxs-lookup"><span data-stu-id="831f7-112">Pointer to a **BSTR** containing the values of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="831f7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="831f7-113">Return value</span></span>

<span data-ttu-id="831f7-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="831f7-114">This method can return one of these values.</span></span>



| <span data-ttu-id="831f7-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="831f7-115">Return code</span></span>                                                                                   | <span data-ttu-id="831f7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="831f7-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="831f7-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="831f7-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="831f7-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="831f7-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="831f7-120">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="831f7-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="831f7-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="831f7-122">Недопустимый параметр *индекса* .</span><span class="sxs-lookup"><span data-stu-id="831f7-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="831f7-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="831f7-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="831f7-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="831f7-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="831f7-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="831f7-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="831f7-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="831f7-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="831f7-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="831f7-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="831f7-129">Remarks</span></span>

<span data-ttu-id="831f7-130">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *Pval* .</span><span class="sxs-lookup"><span data-stu-id="831f7-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *pVal* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="831f7-131">Требования</span><span class="sxs-lookup"><span data-stu-id="831f7-131">Requirements</span></span>



| <span data-ttu-id="831f7-132">Требование</span><span class="sxs-lookup"><span data-stu-id="831f7-132">Requirement</span></span> | <span data-ttu-id="831f7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="831f7-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="831f7-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="831f7-134">TAPI version</span></span><br/> | <span data-ttu-id="831f7-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="831f7-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="831f7-136">Header</span><span class="sxs-lookup"><span data-stu-id="831f7-136">Header</span></span><br/>       | <dl> <span data-ttu-id="831f7-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="831f7-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="831f7-138">Library</span></span><br/>      | <dl> <span data-ttu-id="831f7-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="831f7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="831f7-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="831f7-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="831f7-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="831f7-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="831f7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831f7-143">**итаттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="831f7-143">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

