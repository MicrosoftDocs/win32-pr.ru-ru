---
description: Метод Сетусернаме задает определяемое приложением имя для объекта.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'Метод Иамтимелинеобж:: Сетусернаме (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689136"
---
# <a name="iamtimelineobjsetusername-method"></a><span data-ttu-id="1da00-103">Метод Иамтимелинеобж:: Сетусернаме</span><span class="sxs-lookup"><span data-stu-id="1da00-103">IAMTimelineObj::SetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="1da00-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1da00-104">\[Deprecated.</span></span> <span data-ttu-id="1da00-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1da00-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1da00-106">`SetUserName`Метод задает определяемое приложением имя для объекта.</span><span class="sxs-lookup"><span data-stu-id="1da00-106">The `SetUserName` method sets an application-defined name for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da00-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1da00-107">Syntax</span></span>


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="1da00-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1da00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da00-109">*неввал*</span><span class="sxs-lookup"><span data-stu-id="1da00-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="1da00-110">Строка расширенных символов, содержащая имя.</span><span class="sxs-lookup"><span data-stu-id="1da00-110">Wide-character string that contains the name.</span></span> <span data-ttu-id="1da00-111">Строки длиннее 256 символов могут быть усечены.</span><span class="sxs-lookup"><span data-stu-id="1da00-111">Strings longer than 256 characters might be truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da00-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1da00-112">Return value</span></span>

<span data-ttu-id="1da00-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1da00-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1da00-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1da00-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1da00-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1da00-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1da00-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1da00-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1da00-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1da00-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1da00-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1da00-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1da00-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1da00-119">Requirements</span></span>



| <span data-ttu-id="1da00-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1da00-120">Requirement</span></span> | <span data-ttu-id="1da00-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1da00-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1da00-122">Header</span><span class="sxs-lookup"><span data-stu-id="1da00-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1da00-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1da00-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1da00-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1da00-124">Library</span></span><br/> | <dl> <span data-ttu-id="1da00-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1da00-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1da00-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1da00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da00-127">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="1da00-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="1da00-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="1da00-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




