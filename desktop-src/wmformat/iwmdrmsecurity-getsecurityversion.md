---
title: Метод Ивмдрмсекурити Жетсекуритиверсион (Вмдрмсдк. h)
description: Метод Жетсекуритиверсион извлекает версию подсистемы DRM на клиентском компьютере.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Формат Windows Media, Жетсекуритиверсион метод
- Жетсекуритиверсион метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Жетсекуритиверсион
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665481"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a><span data-ttu-id="62209-106">Метод Ивмдрмсекурити:: Жетсекуритиверсион</span><span class="sxs-lookup"><span data-stu-id="62209-106">IWMDRMSecurity::GetSecurityVersion method</span></span>

<span data-ttu-id="62209-107">Метод **жетсекуритиверсион** извлекает версию подсистемы DRM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="62209-107">The **GetSecurityVersion** method retrieves the version of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="62209-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62209-108">Syntax</span></span>


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a><span data-ttu-id="62209-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="62209-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62209-110">*пбстрверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="62209-110">*pbstrVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62209-111">Адрес переменной, которая получает номер версии подсистемы DRM.</span><span class="sxs-lookup"><span data-stu-id="62209-111">Address of a variable that receives the DRM subsystem version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62209-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62209-112">Return value</span></span>

<span data-ttu-id="62209-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="62209-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="62209-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="62209-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="62209-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="62209-115">Return code</span></span>                                                                          | <span data-ttu-id="62209-116">Описание</span><span class="sxs-lookup"><span data-stu-id="62209-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="62209-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="62209-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="62209-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="62209-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62209-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62209-119">Remarks</span></span>

<span data-ttu-id="62209-120">Номер версии выражается в виде строки, состоящей из четырех чисел, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="62209-120">The version number is expressed as a string consisting of four numbers separated by periods.</span></span> <span data-ttu-id="62209-121">Первое число — основной номер версии, который обычно имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="62209-121">The first number is the major version number, which is usually set to 2.</span></span> <span data-ttu-id="62209-122">Второе число — это дополнительный номер версии в диапазоне от 2 до 10.</span><span class="sxs-lookup"><span data-stu-id="62209-122">The second number is the minor version number, ranging from 2 to 10.</span></span> <span data-ttu-id="62209-123">Третье число всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="62209-123">The third number is always set to 0.</span></span> <span data-ttu-id="62209-124">Четвертое число устанавливается в 0 или 1, а является логическим значением, указывающим, является ли подсистема индивидуальной.</span><span class="sxs-lookup"><span data-stu-id="62209-124">The fourth number is set to 0 or 1, and is a Boolean value indicating whether the subsystem has been individualized.</span></span> <span data-ttu-id="62209-125">Например, номер версии "2.4.0.1" указывает на отдельную четвертую младшую версию второй основной версии.</span><span class="sxs-lookup"><span data-stu-id="62209-125">For example, a version number of "2.4.0.1" indicates the individualized fourth minor version of the second major version.</span></span>

## <a name="requirements"></a><span data-ttu-id="62209-126">Требования</span><span class="sxs-lookup"><span data-stu-id="62209-126">Requirements</span></span>



| <span data-ttu-id="62209-127">Требование</span><span class="sxs-lookup"><span data-stu-id="62209-127">Requirement</span></span> | <span data-ttu-id="62209-128">Значение</span><span class="sxs-lookup"><span data-stu-id="62209-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62209-129">Header</span><span class="sxs-lookup"><span data-stu-id="62209-129">Header</span></span><br/>  | <dl> <span data-ttu-id="62209-130"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="62209-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="62209-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62209-131">Library</span></span><br/> | <dl> <span data-ttu-id="62209-132"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62209-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62209-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62209-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62209-134">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="62209-134">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





