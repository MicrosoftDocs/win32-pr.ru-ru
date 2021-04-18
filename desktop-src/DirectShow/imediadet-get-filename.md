---
description: Метод Get \_ filename извлекает имя исходного файла, который в настоящее время используется средством обнаружения мультимедиа.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'Метод Имедиадет:: get_Filename (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95a350dde3dfdc1c6046c8e31b8a2d9e62684788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675981"
---
# <a name="imediadetget_filename-method"></a><span data-ttu-id="4699f-103">Метод Имедиадет:: Get \_ имя_файла</span><span class="sxs-lookup"><span data-stu-id="4699f-103">IMediaDet::get\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="4699f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4699f-104">\[Deprecated.</span></span> <span data-ttu-id="4699f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4699f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4699f-106">`get_Filename`Метод получает имя исходного файла, который в настоящее время используется средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4699f-106">The `get_Filename` method retrieves the name of the source file currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="4699f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4699f-107">Syntax</span></span>


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4699f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4699f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4699f-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4699f-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4699f-110">Получает имя файла.</span><span class="sxs-lookup"><span data-stu-id="4699f-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4699f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4699f-111">Return value</span></span>

<span data-ttu-id="4699f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4699f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4699f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4699f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4699f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4699f-114">Remarks</span></span>

<span data-ttu-id="4699f-115">Метод выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="4699f-115">The method allocates memory for the string.</span></span> <span data-ttu-id="4699f-116">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="4699f-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="4699f-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4699f-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4699f-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4699f-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4699f-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4699f-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4699f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4699f-120">Requirements</span></span>



| <span data-ttu-id="4699f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4699f-121">Requirement</span></span> | <span data-ttu-id="4699f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4699f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4699f-123">Header</span><span class="sxs-lookup"><span data-stu-id="4699f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4699f-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4699f-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4699f-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4699f-125">Library</span></span><br/> | <dl> <span data-ttu-id="4699f-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4699f-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4699f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4699f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4699f-128">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="4699f-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="4699f-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="4699f-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




