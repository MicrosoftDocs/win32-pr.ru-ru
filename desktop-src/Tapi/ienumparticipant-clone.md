---
description: Метод Clone создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий. Этот метод скрыт от Visual Basic и языков сценариев.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'Метод ИенумпартиЦипант:: Clone (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679957"
---
# <a name="ienumparticipantclone-method"></a><span data-ttu-id="f56e6-104">Метод ИенумпартиЦипант:: Clone</span><span class="sxs-lookup"><span data-stu-id="f56e6-104">IEnumParticipant::Clone method</span></span>

<span data-ttu-id="f56e6-105">\[**Клон** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f56e6-105">\[**Clone** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f56e6-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f56e6-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f56e6-107">Метод **clone** создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="f56e6-107">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span> <span data-ttu-id="f56e6-108">Этот метод скрыт от Visual Basic и языков сценариев.</span><span class="sxs-lookup"><span data-stu-id="f56e6-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56e6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f56e6-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="f56e6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f56e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f56e6-111">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f56e6-111">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f56e6-112">Указатель на новый интерфейс [**иенумпартиЦипант**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="f56e6-112">Pointer to new [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f56e6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f56e6-113">Return value</span></span>

<span data-ttu-id="f56e6-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f56e6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f56e6-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f56e6-115">Return code</span></span>                                                                                   | <span data-ttu-id="f56e6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f56e6-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f56e6-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f56e6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f56e6-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f56e6-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f56e6-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f56e6-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f56e6-120">Параметр *ппенум* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="f56e6-120">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="f56e6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f56e6-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f56e6-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f56e6-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f56e6-123"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="f56e6-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="f56e6-124">Сбой по неизвестным причинам.</span><span class="sxs-lookup"><span data-stu-id="f56e6-124">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="f56e6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f56e6-125">Remarks</span></span>

<span data-ttu-id="f56e6-126">TAPI вызывает метод [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) в интерфейсе [**иенумпартиЦипант**](ienumparticipant.md) , возвращенном **иенумпартиЦипант:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="f56e6-126">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **IEnumParticipant::Clone**.</span></span> <span data-ttu-id="f56e6-127">Приложение должно вызвать [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) в интерфейсе **иенумпартиЦипант** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="f56e6-127">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f56e6-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f56e6-128">Requirements</span></span>



| <span data-ttu-id="f56e6-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f56e6-129">Requirement</span></span> | <span data-ttu-id="f56e6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f56e6-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f56e6-131">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f56e6-131">TAPI version</span></span><br/> | <span data-ttu-id="f56e6-132">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f56e6-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f56e6-133">Header</span><span class="sxs-lookup"><span data-stu-id="f56e6-133">Header</span></span><br/>       | <dl> <span data-ttu-id="f56e6-134"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="f56e6-134"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f56e6-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f56e6-135">Library</span></span><br/>      | <dl> <span data-ttu-id="f56e6-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f56e6-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f56e6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f56e6-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="f56e6-138"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f56e6-138"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f56e6-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f56e6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f56e6-140">**иенумпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="f56e6-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="f56e6-141">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="f56e6-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

