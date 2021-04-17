---
description: Метод Скрапит отклоняет граф фильтра механизма отрисовки и все связанные объекты.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'Метод Ирендеренгине:: Скрапит (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679887"
---
# <a name="irenderenginescrapit-method"></a><span data-ttu-id="9f773-103">Метод Ирендеренгине:: Скрапит</span><span class="sxs-lookup"><span data-stu-id="9f773-103">IRenderEngine::ScrapIt method</span></span>

> [!Note]  
> <span data-ttu-id="9f773-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9f773-104">\[Deprecated.</span></span> <span data-ttu-id="9f773-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f773-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f773-106">`ScrapIt`Метод отклоняет граф фильтра механизма отрисовки и все связанные объекты.</span><span class="sxs-lookup"><span data-stu-id="9f773-106">The `ScrapIt` method discards the render engine's filter graph and all associated objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f773-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f773-107">Syntax</span></span>


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a><span data-ttu-id="9f773-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f773-108">Parameters</span></span>

<span data-ttu-id="9f773-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9f773-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f773-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f773-110">Return value</span></span>

<span data-ttu-id="9f773-111">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="9f773-111">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="9f773-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9f773-112">Return code</span></span>                                                                                            | <span data-ttu-id="9f773-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9f773-113">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9f773-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9f773-114"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="9f773-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="9f773-115">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="9f773-116"><dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt></span><span class="sxs-lookup"><span data-stu-id="9f773-116"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="9f773-117">Не удалось инициализировать модуль визуализации.</span><span class="sxs-lookup"><span data-stu-id="9f773-117">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9f773-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f773-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f773-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9f773-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f773-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f773-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9f773-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9f773-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f773-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9f773-122">Requirements</span></span>



| <span data-ttu-id="9f773-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9f773-123">Requirement</span></span> | <span data-ttu-id="9f773-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9f773-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f773-125">Header</span><span class="sxs-lookup"><span data-stu-id="9f773-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9f773-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f773-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9f773-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f773-127">Library</span></span><br/> | <dl> <span data-ttu-id="9f773-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f773-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f773-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f773-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f773-130">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="9f773-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="9f773-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="9f773-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




