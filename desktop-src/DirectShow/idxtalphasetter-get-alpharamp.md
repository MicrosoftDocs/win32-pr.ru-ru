---
description: Метод Get \_ алфарамп извлекает свойство alpha пандус. Альфа-шкала — это процентная доля, на которую корректируются значения альфа в исходном изображении. Например, если альфа-пандус имеет значение 0,5, то значения альфа в изображении уменьшаются на 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Метод Идксталфасеттер:: get_AlphaRamp (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685367"
---
# <a name="idxtalphasetterget_alpharamp-method"></a><span data-ttu-id="1eab1-105">Метод Идксталфасеттер:: Get \_ алфарамп</span><span class="sxs-lookup"><span data-stu-id="1eab1-105">IDxtAlphaSetter::get\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="1eab1-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1eab1-106">\[Deprecated.</span></span> <span data-ttu-id="1eab1-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1eab1-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1eab1-108">`get_AlphaRamp`Метод извлекает свойство alpha пандус.</span><span class="sxs-lookup"><span data-stu-id="1eab1-108">The `get_AlphaRamp` method retrieves the alpha ramp property.</span></span> <span data-ttu-id="1eab1-109">Альфа-шкала — это процентная доля, на которую корректируются значения альфа в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="1eab1-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="1eab1-110">Например, если альфа-пандус имеет значение 0,5, то значения альфа в изображении уменьшаются на 50%.</span><span class="sxs-lookup"><span data-stu-id="1eab1-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eab1-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eab1-111">Syntax</span></span>


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="1eab1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eab1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eab1-113">*палфа* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1eab1-113">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab1-114">Получает альфа-пандус.</span><span class="sxs-lookup"><span data-stu-id="1eab1-114">Receives the alpha ramp.</span></span> <span data-ttu-id="1eab1-115">Отрицательное значение указывает, что альфа-шкала не задана.</span><span class="sxs-lookup"><span data-stu-id="1eab1-115">A negative value indicates that no alpha ramp is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eab1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eab1-116">Return value</span></span>

<span data-ttu-id="1eab1-117">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1eab1-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1eab1-118">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="1eab1-118">Possible values include the following.</span></span>



| <span data-ttu-id="1eab1-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1eab1-119">Return code</span></span>                                                                               | <span data-ttu-id="1eab1-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1eab1-120">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="1eab1-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1eab1-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="1eab1-122">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="1eab1-122">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="1eab1-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1eab1-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1eab1-124">Успешно</span><span class="sxs-lookup"><span data-stu-id="1eab1-124">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="1eab1-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eab1-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1eab1-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1eab1-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1eab1-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1eab1-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1eab1-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1eab1-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1eab1-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1eab1-129">Requirements</span></span>



| <span data-ttu-id="1eab1-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1eab1-130">Requirement</span></span> | <span data-ttu-id="1eab1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1eab1-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eab1-132">Header</span><span class="sxs-lookup"><span data-stu-id="1eab1-132">Header</span></span><br/>  | <dl> <span data-ttu-id="1eab1-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eab1-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1eab1-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1eab1-134">Library</span></span><br/> | <dl> <span data-ttu-id="1eab1-135"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eab1-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eab1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eab1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eab1-137">**Интерфейс Идксталфасеттер**</span><span class="sxs-lookup"><span data-stu-id="1eab1-137">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




