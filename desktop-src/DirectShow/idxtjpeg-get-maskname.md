---
description: Метод Get \_ маскнаме извлекает имя JPEG-файла, который будет использоваться в качестве маски очистки.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Метод Идкстжпег:: get_MaskName (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675118"
---
# <a name="idxtjpegget_maskname-method"></a><span data-ttu-id="8f572-103">Метод Идкстжпег:: Get \_ маскнаме</span><span class="sxs-lookup"><span data-stu-id="8f572-103">IDxtJpeg::get\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="8f572-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8f572-104">\[Deprecated.</span></span> <span data-ttu-id="8f572-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f572-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8f572-106">`get_MaskName`Метод получает имя JPEG-файла, который будет использоваться в качестве маски очистки.</span><span class="sxs-lookup"><span data-stu-id="8f572-106">The `get_MaskName` method retrieves the name of a JPEG file to be used as the wipe mask.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f572-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f572-107">Syntax</span></span>


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8f572-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f572-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f572-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8f572-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8f572-110">Получает имя файла.</span><span class="sxs-lookup"><span data-stu-id="8f572-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f572-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f572-111">Return value</span></span>

<span data-ttu-id="8f572-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8f572-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f572-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f572-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f572-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f572-114">Remarks</span></span>

<span data-ttu-id="8f572-115">Если переход на очистку использует одну из встроенных SMPTE для очистки, то значением этого свойства является пустая строка.</span><span class="sxs-lookup"><span data-stu-id="8f572-115">If the wipe transition is using one of the built-in SMPTE wipes that it supports, the value of this property is an empty string.</span></span>

<span data-ttu-id="8f572-116">Вызывающий объект должен освободить возвращенную строку с помощью функции **сисфристринг** .</span><span class="sxs-lookup"><span data-stu-id="8f572-116">The caller must release the returned string, using the **SysFreeString** function.</span></span>

> [!Note]  
> <span data-ttu-id="8f572-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="8f572-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8f572-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8f572-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8f572-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8f572-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8f572-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8f572-120">Requirements</span></span>



| <span data-ttu-id="8f572-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8f572-121">Requirement</span></span> | <span data-ttu-id="8f572-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8f572-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f572-123">Header</span><span class="sxs-lookup"><span data-stu-id="8f572-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8f572-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f572-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8f572-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f572-125">Library</span></span><br/> | <dl> <span data-ttu-id="8f572-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f572-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f572-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f572-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f572-128">**Интерфейс Идкстжпег**</span><span class="sxs-lookup"><span data-stu-id="8f572-128">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="8f572-129">**Идкстжпег:: Get \_ маскнум**</span><span class="sxs-lookup"><span data-stu-id="8f572-129">**IDxtJpeg::get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




