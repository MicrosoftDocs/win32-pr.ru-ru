---
description: Следующий метод получает указанное число следующих элементов в последовательности перечисления. Этот метод скрыт от Visual Basic и языков сценариев.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'Метод ИенумпартиЦипант:: Next (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689432"
---
# <a name="ienumparticipantnext-method"></a><span data-ttu-id="d9260-104">Метод ИенумпартиЦипант:: Next</span><span class="sxs-lookup"><span data-stu-id="d9260-104">IEnumParticipant::Next method</span></span>

<span data-ttu-id="d9260-105">\[Команда **Далее** недоступна для Windows Vista, windows Server 2008 и последующих версий операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d9260-105">\[**Next** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d9260-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="d9260-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d9260-107">**Следующий** метод получает указанное число следующих элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="d9260-107">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="d9260-108">Этот метод скрыт от Visual Basic и языков сценариев.</span><span class="sxs-lookup"><span data-stu-id="d9260-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9260-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9260-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d9260-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9260-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9260-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9260-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9260-112">Число запрошенных элементов.</span><span class="sxs-lookup"><span data-stu-id="d9260-112">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="d9260-113">*ппелементс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9260-113">*ppElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9260-114">Указатель на интерфейсы [**итаженсандлер**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .</span><span class="sxs-lookup"><span data-stu-id="d9260-114">Pointer to [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="d9260-115">*пцелтфетчед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9260-115">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9260-116">Фактически предоставляемый указатель на число элементов.</span><span class="sxs-lookup"><span data-stu-id="d9260-116">Pointer to number of elements actually supplied.</span></span> <span data-ttu-id="d9260-117">Может иметь **значение NULL** , если значение *celt* равно единице.</span><span class="sxs-lookup"><span data-stu-id="d9260-117">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9260-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9260-118">Return value</span></span>

<span data-ttu-id="d9260-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d9260-119">This method can return one of these values.</span></span>



| <span data-ttu-id="d9260-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d9260-120">Return code</span></span>                                                                                   | <span data-ttu-id="d9260-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d9260-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d9260-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d9260-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d9260-123">Метод возвратил *celt* число элементов.</span><span class="sxs-lookup"><span data-stu-id="d9260-123">Method returned *celt* number of elements.</span></span><br/>           |
| <dl> <span data-ttu-id="d9260-124"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d9260-124"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="d9260-125">Количество оставшихся элементов меньше значения *celt*.</span><span class="sxs-lookup"><span data-stu-id="d9260-125">Number of elements remaining was less than *celt*.</span></span><br/>   |
| <dl> <span data-ttu-id="d9260-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="d9260-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d9260-127">Параметр *ппелементс* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="d9260-127">The *ppElements* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="d9260-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d9260-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d9260-129">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="d9260-129">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9260-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9260-130">Remarks</span></span>

<span data-ttu-id="d9260-131">TAPI вызывает метод [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) в интерфейсе [**итаженсандлер**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) , возвращенном методом **иенумпартиЦипант:: Next**.</span><span class="sxs-lookup"><span data-stu-id="d9260-131">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interface returned by **IEnumParticipant::Next**.</span></span> <span data-ttu-id="d9260-132">Приложение должно вызвать [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) в интерфейсе **итаженсандлер** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="d9260-132">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **ITAgentHandler** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9260-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d9260-133">Requirements</span></span>



| <span data-ttu-id="d9260-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d9260-134">Requirement</span></span> | <span data-ttu-id="d9260-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d9260-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9260-136">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d9260-136">TAPI version</span></span><br/> | <span data-ttu-id="d9260-137">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d9260-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d9260-138">Header</span><span class="sxs-lookup"><span data-stu-id="d9260-138">Header</span></span><br/>       | <dl> <span data-ttu-id="d9260-139"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9260-139"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="d9260-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9260-140">Library</span></span><br/>      | <dl> <span data-ttu-id="d9260-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9260-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d9260-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d9260-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="d9260-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9260-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d9260-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9260-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9260-145">**иенумпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="d9260-145">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="d9260-146">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="d9260-146">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

