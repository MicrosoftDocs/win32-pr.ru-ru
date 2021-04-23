---
description: Не поддерживается.
ms.assetid: 4fd6b9d9-1749-44e6-884a-16faeced4ed6
title: 'Метод Иамтимелинеграуп:: Исрекомпрессформатдирти (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsRecompressFormatDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b1e395c46149f1ab63afebbbf08bd462726ba19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688905"
---
# <a name="iamtimelinegroupisrecompressformatdirty-method"></a><span data-ttu-id="f8cf6-103">Метод Иамтимелинеграуп:: Исрекомпрессформатдирти</span><span class="sxs-lookup"><span data-stu-id="f8cf6-103">IAMTimelineGroup::IsRecompressFormatDirty method</span></span>

> [!Note]  
> <span data-ttu-id="f8cf6-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f8cf6-104">\[Deprecated.</span></span> <span data-ttu-id="f8cf6-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f8cf6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f8cf6-106">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8cf6-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8cf6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8cf6-107">Syntax</span></span>


```C++
HRESULT IsRecompressFormatDirty(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f8cf6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8cf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8cf6-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="f8cf6-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f8cf6-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f8cf6-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8cf6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8cf6-111">Return value</span></span>

<span data-ttu-id="f8cf6-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8cf6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8cf6-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8cf6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8cf6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8cf6-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8cf6-115">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="f8cf6-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f8cf6-116">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f8cf6-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f8cf6-117">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f8cf6-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8cf6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f8cf6-118">Requirements</span></span>



| <span data-ttu-id="f8cf6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f8cf6-119">Requirement</span></span> | <span data-ttu-id="f8cf6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f8cf6-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cf6-121">Header</span><span class="sxs-lookup"><span data-stu-id="f8cf6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f8cf6-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8cf6-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f8cf6-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8cf6-123">Library</span></span><br/> | <dl> <span data-ttu-id="f8cf6-124"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8cf6-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8cf6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8cf6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cf6-126">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="f8cf6-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




