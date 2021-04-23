---
description: Метод WriteXML преобразует временную шкалу в XML-строку.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'Метод IXml2Dex:: WriteXML (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674971"
---
# <a name="ixml2dexwritexml-method"></a><span data-ttu-id="e6e51-103">Метод IXml2Dex:: WriteXML</span><span class="sxs-lookup"><span data-stu-id="e6e51-103">IXml2Dex::WriteXML method</span></span>

> [!Note]  
> <span data-ttu-id="e6e51-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e6e51-104">\[Deprecated.</span></span> <span data-ttu-id="e6e51-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6e51-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6e51-106">`WriteXML`Метод преобразует временную шкалу в XML-строку.</span><span class="sxs-lookup"><span data-stu-id="e6e51-106">The `WriteXML` method translates a timeline to an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6e51-107">Syntax</span></span>


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a><span data-ttu-id="e6e51-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6e51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e51-109">*птимелине*</span><span class="sxs-lookup"><span data-stu-id="e6e51-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e51-110">Указатель на интерфейс **IUnknown** объекта временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="e6e51-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="e6e51-111">*пбстрксмл*</span><span class="sxs-lookup"><span data-stu-id="e6e51-111">*pbstrXML*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e51-112">Указатель на переменную типа BSTR, которая получает XML-строку, описывающую временную шкалу.</span><span class="sxs-lookup"><span data-stu-id="e6e51-112">Pointer to a variable of type BSTR that receives the XML string describing the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e51-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6e51-113">Return value</span></span>

<span data-ttu-id="e6e51-114">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="e6e51-114">Returns S\_OK if successful.</span></span> <span data-ttu-id="e6e51-115">При нехватке памяти для преобразования возвращает E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e6e51-115">If there is insufficient memory for the conversion, returns E\_OUTOFMEMORY.</span></span> <span data-ttu-id="e6e51-116">В противном случае возвращает другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e6e51-116">Otherwise, returns another error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e51-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6e51-117">Remarks</span></span>

<span data-ttu-id="e6e51-118">Метод выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="e6e51-118">The method allocates memory for the string.</span></span> <span data-ttu-id="e6e51-119">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="e6e51-119">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="e6e51-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="e6e51-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6e51-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6e51-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6e51-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e6e51-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6e51-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e6e51-123">Requirements</span></span>



| <span data-ttu-id="e6e51-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e6e51-124">Requirement</span></span> | <span data-ttu-id="e6e51-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e6e51-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e51-126">Версия</span><span class="sxs-lookup"><span data-stu-id="e6e51-126">Version</span></span><br/> | <span data-ttu-id="e6e51-127">Internet Explorer 4,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e6e51-127">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="e6e51-128">Header</span><span class="sxs-lookup"><span data-stu-id="e6e51-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e6e51-129"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e51-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6e51-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6e51-130">Library</span></span><br/> | <dl> <span data-ttu-id="e6e51-131"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6e51-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e51-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6e51-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e51-133">**Интерфейс IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="e6e51-133">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="e6e51-134">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="e6e51-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




