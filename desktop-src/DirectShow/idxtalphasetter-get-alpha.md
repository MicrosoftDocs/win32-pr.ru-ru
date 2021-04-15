---
description: Метод Get \_ Alpha извлекает альфа-значение для всего изображения.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Метод Идксталфасеттер:: get_Alpha (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688802"
---
# <a name="idxtalphasetterget_alpha-method"></a><span data-ttu-id="346e9-103">Метод Идксталфасеттер:: Get \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="346e9-103">IDxtAlphaSetter::get\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="346e9-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="346e9-104">\[Deprecated.</span></span> <span data-ttu-id="346e9-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="346e9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="346e9-106">`get_Alpha`Метод получает альфа-значение для всего изображения.</span><span class="sxs-lookup"><span data-stu-id="346e9-106">The `get_Alpha` method retrieves the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="346e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="346e9-107">Syntax</span></span>


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="346e9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="346e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="346e9-109">*палфа* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="346e9-109">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="346e9-110">Получает альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="346e9-110">Receives the alpha value.</span></span> <span data-ttu-id="346e9-111">Это альфа-значение будет применено ко всему целевому образу.</span><span class="sxs-lookup"><span data-stu-id="346e9-111">This alpha value will be applied to the entire target image.</span></span> <span data-ttu-id="346e9-112">Отрицательное значение указывает, что альфа-значение не задано.</span><span class="sxs-lookup"><span data-stu-id="346e9-112">A negative value indicates that no alpha value is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="346e9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="346e9-113">Return value</span></span>

<span data-ttu-id="346e9-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="346e9-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="346e9-115">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="346e9-115">Possible values include the following.</span></span>



| <span data-ttu-id="346e9-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="346e9-116">Return code</span></span>                                                                               | <span data-ttu-id="346e9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="346e9-117">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="346e9-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="346e9-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="346e9-119">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="346e9-119">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="346e9-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="346e9-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="346e9-121">Успешно</span><span class="sxs-lookup"><span data-stu-id="346e9-121">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="346e9-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="346e9-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="346e9-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="346e9-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="346e9-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="346e9-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="346e9-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="346e9-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="346e9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="346e9-126">Requirements</span></span>



| <span data-ttu-id="346e9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="346e9-127">Requirement</span></span> | <span data-ttu-id="346e9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="346e9-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="346e9-129">Header</span><span class="sxs-lookup"><span data-stu-id="346e9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="346e9-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="346e9-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="346e9-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="346e9-131">Library</span></span><br/> | <dl> <span data-ttu-id="346e9-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="346e9-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346e9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="346e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346e9-134">**Интерфейс Идксталфасеттер**</span><span class="sxs-lookup"><span data-stu-id="346e9-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




