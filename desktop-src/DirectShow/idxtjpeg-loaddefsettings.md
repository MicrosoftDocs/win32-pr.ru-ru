---
description: Метод Лоаддефсеттингс восстанавливает параметры по умолчанию для перехода на очистку.
ms.assetid: 3f81002a-ecac-4d5a-8d2a-ada4d4884d7d
title: 'Метод Идкстжпег:: Лоаддефсеттингс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.LoadDefSettings
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51438a21782d1a703a3b43134517e8337ce9f75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675982"
---
# <a name="idxtjpegloaddefsettings-method"></a><span data-ttu-id="9f728-103">Метод Идкстжпег:: Лоаддефсеттингс</span><span class="sxs-lookup"><span data-stu-id="9f728-103">IDxtJpeg::LoadDefSettings method</span></span>

> [!Note]  
> <span data-ttu-id="9f728-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9f728-104">\[Deprecated.</span></span> <span data-ttu-id="9f728-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f728-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f728-106">`LoadDefSettings`Метод восстанавливает параметры по умолчанию для перехода на очистку.</span><span class="sxs-lookup"><span data-stu-id="9f728-106">The `LoadDefSettings` method restores the default settings of the Wipe transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f728-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f728-107">Syntax</span></span>


```C++
HRESULT LoadDefSettings();
```



## <a name="parameters"></a><span data-ttu-id="9f728-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f728-108">Parameters</span></span>

<span data-ttu-id="9f728-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9f728-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f728-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f728-110">Return value</span></span>

<span data-ttu-id="9f728-111">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9f728-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f728-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f728-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f728-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f728-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f728-114">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9f728-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f728-115">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f728-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9f728-116">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9f728-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f728-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9f728-117">Requirements</span></span>



| <span data-ttu-id="9f728-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9f728-118">Requirement</span></span> | <span data-ttu-id="9f728-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9f728-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f728-120">Header</span><span class="sxs-lookup"><span data-stu-id="9f728-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9f728-121"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f728-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9f728-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f728-122">Library</span></span><br/> | <dl> <span data-ttu-id="9f728-123"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f728-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f728-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f728-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f728-125">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="9f728-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




