---
description: Метод UserData извлекает определяемые приложением постоянные данные.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'Метод Иамтимелинеобж:: UserData (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679719"
---
# <a name="iamtimelineobjgetuserdata-method"></a><span data-ttu-id="8b150-103">Метод Иамтимелинеобж:: UserData</span><span class="sxs-lookup"><span data-stu-id="8b150-103">IAMTimelineObj::GetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="8b150-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8b150-104">\[Deprecated.</span></span> <span data-ttu-id="8b150-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b150-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8b150-106">`GetUserData`Метод получает определяемые приложением постоянные данные.</span><span class="sxs-lookup"><span data-stu-id="8b150-106">The `GetUserData` method retrieves the application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b150-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b150-107">Syntax</span></span>


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="8b150-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b150-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b150-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="8b150-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="8b150-110">Указатель на буфер, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="8b150-110">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="8b150-111">Чтобы определить размер выделяемого буфера, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8b150-111">To determine the size of buffer to allocate, set this parameter to **NULL**.</span></span> <span data-ttu-id="8b150-112">Требуемый размер возвращается в *псизе*.</span><span class="sxs-lookup"><span data-stu-id="8b150-112">The required size is returned in *pSize*.</span></span>

</dd> <dt>

<span data-ttu-id="8b150-113">*псизе*</span><span class="sxs-lookup"><span data-stu-id="8b150-113">*pSize*</span></span> 
</dt> <dd>

<span data-ttu-id="8b150-114">Получает размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="8b150-114">Receives the size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b150-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b150-115">Return value</span></span>

<span data-ttu-id="8b150-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8b150-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b150-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b150-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b150-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b150-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b150-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="8b150-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8b150-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8b150-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8b150-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8b150-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b150-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8b150-122">Requirements</span></span>



| <span data-ttu-id="8b150-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8b150-123">Requirement</span></span> | <span data-ttu-id="8b150-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8b150-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b150-125">Header</span><span class="sxs-lookup"><span data-stu-id="8b150-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8b150-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b150-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8b150-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b150-127">Library</span></span><br/> | <dl> <span data-ttu-id="8b150-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b150-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b150-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b150-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b150-130">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="8b150-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="8b150-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="8b150-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




