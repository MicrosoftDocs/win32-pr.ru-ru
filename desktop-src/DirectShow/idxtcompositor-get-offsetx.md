---
description: Метод Get \_ оффсеткс извлекает горизонтальное смещение целевого прямоугольника.
ms.assetid: a9d8c81b-f978-4b47-9c7f-12cee7c2c40d
title: 'Метод Идксткомпоситор:: get_OffsetX (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8e2f21956e67b42158f4e646d33aa6e3e90d9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679803"
---
# <a name="idxtcompositorget_offsetx-method"></a><span data-ttu-id="146c9-103">Метод Идксткомпоситор:: Get \_ оффсеткс</span><span class="sxs-lookup"><span data-stu-id="146c9-103">IDxtCompositor::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="146c9-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="146c9-104">\[Deprecated.</span></span> <span data-ttu-id="146c9-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="146c9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="146c9-106">`get_OffsetX`Метод получает горизонтальное смещение целевого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="146c9-106">The `get_OffsetX` method retrieves the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="146c9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="146c9-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="146c9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="146c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="146c9-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="146c9-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="146c9-110">Получает горизонтальное смещение целевого прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="146c9-110">Receives the horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="146c9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="146c9-111">Return value</span></span>

<span data-ttu-id="146c9-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="146c9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="146c9-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="146c9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="146c9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="146c9-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="146c9-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="146c9-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="146c9-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="146c9-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="146c9-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="146c9-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="146c9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="146c9-118">Requirements</span></span>



| <span data-ttu-id="146c9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="146c9-119">Requirement</span></span> | <span data-ttu-id="146c9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="146c9-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="146c9-121">Header</span><span class="sxs-lookup"><span data-stu-id="146c9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="146c9-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="146c9-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="146c9-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="146c9-123">Library</span></span><br/> | <dl> <span data-ttu-id="146c9-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="146c9-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="146c9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="146c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="146c9-126">**Интерфейс Идксткомпоситор**</span><span class="sxs-lookup"><span data-stu-id="146c9-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




