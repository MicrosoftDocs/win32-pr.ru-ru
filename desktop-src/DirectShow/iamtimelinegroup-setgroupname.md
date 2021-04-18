---
description: Метод Сетграупнаме задает определяемое приложением имя группы.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'Метод Иамтимелинеграуп:: Сетграупнаме (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685220"
---
# <a name="iamtimelinegroupsetgroupname-method"></a><span data-ttu-id="2c228-103">Метод Иамтимелинеграуп:: Сетграупнаме</span><span class="sxs-lookup"><span data-stu-id="2c228-103">IAMTimelineGroup::SetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="2c228-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2c228-104">\[Deprecated.</span></span> <span data-ttu-id="2c228-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2c228-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2c228-106">`SetGroupName`Метод задает определяемое приложением имя группы.</span><span class="sxs-lookup"><span data-stu-id="2c228-106">The `SetGroupName` method sets the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c228-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c228-107">Syntax</span></span>


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="2c228-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c228-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c228-109">*пграупнаме*</span><span class="sxs-lookup"><span data-stu-id="2c228-109">*pGroupName*</span></span> 
</dt> <dd>

<span data-ttu-id="2c228-110">**BSTR** , указывающий имя группы.</span><span class="sxs-lookup"><span data-stu-id="2c228-110">**BSTR** that specifies the name of the group.</span></span> <span data-ttu-id="2c228-111">Максимальная длина имени — 256 символов, инкудинг терминатор null.</span><span class="sxs-lookup"><span data-stu-id="2c228-111">The maximum length of the name is 256 characters, incuding the null terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c228-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c228-112">Return value</span></span>

<span data-ttu-id="2c228-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2c228-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c228-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c228-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c228-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c228-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c228-116">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2c228-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2c228-117">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2c228-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2c228-118">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2c228-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c228-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2c228-119">Requirements</span></span>



| <span data-ttu-id="2c228-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2c228-120">Requirement</span></span> | <span data-ttu-id="2c228-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2c228-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c228-122">Header</span><span class="sxs-lookup"><span data-stu-id="2c228-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2c228-123"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c228-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2c228-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c228-124">Library</span></span><br/> | <dl> <span data-ttu-id="2c228-125"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c228-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c228-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c228-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c228-127">**Интерфейс Иамтимелинеграуп**</span><span class="sxs-lookup"><span data-stu-id="2c228-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="2c228-128">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="2c228-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




