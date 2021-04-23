---
description: Метод Where \_ filename указывает имя исходного файла, который будет использоваться средством обнаружения мультимедиа.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: 'Имедиадет: метод ut_Filename:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675439"
---
# <a name="imediadetput_filename-method"></a><span data-ttu-id="e02a7-103">Имедиадет::p \_ методу UT filename</span><span class="sxs-lookup"><span data-stu-id="e02a7-103">IMediaDet::put\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="e02a7-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e02a7-104">\[Deprecated.</span></span> <span data-ttu-id="e02a7-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e02a7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e02a7-106">`put_Filename`Метод задает имя исходного файла для использования средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e02a7-106">The `put_Filename` method specifies the name of the source file for the media detector to use.</span></span>

<span data-ttu-id="e02a7-107">Не вызывайте этот метод дважды для того же объекта Медиадет.</span><span class="sxs-lookup"><span data-stu-id="e02a7-107">Do not call this method twice on the same MediaDet object.</span></span> <span data-ttu-id="e02a7-108">Чтобы использовать этот интерфейс с более чем одним исходным файлом, создайте отдельные экземпляры объекта Медиадет.</span><span class="sxs-lookup"><span data-stu-id="e02a7-108">To use this interface with more than one source file, create separate instances of the MediaDet object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e02a7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e02a7-109">Syntax</span></span>


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e02a7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e02a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e02a7-111">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e02a7-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e02a7-112">Имя файла источника.</span><span class="sxs-lookup"><span data-stu-id="e02a7-112">File name of the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e02a7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e02a7-113">Return value</span></span>

<span data-ttu-id="e02a7-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e02a7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e02a7-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e02a7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e02a7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e02a7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e02a7-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="e02a7-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e02a7-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e02a7-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e02a7-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e02a7-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e02a7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e02a7-120">Requirements</span></span>



| <span data-ttu-id="e02a7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e02a7-121">Requirement</span></span> | <span data-ttu-id="e02a7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e02a7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e02a7-123">Header</span><span class="sxs-lookup"><span data-stu-id="e02a7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e02a7-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="e02a7-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e02a7-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e02a7-125">Library</span></span><br/> | <dl> <span data-ttu-id="e02a7-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e02a7-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e02a7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e02a7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e02a7-128">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="e02a7-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="e02a7-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="e02a7-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




