---
description: Метод Вритексмлфиле преобразует временную шкалу в XML и записывает XML-данные в файл.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'Метод IXml2Dex:: Вритексмлфиле (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689331"
---
# <a name="ixml2dexwritexmlfile-method"></a><span data-ttu-id="490ba-103">Метод IXml2Dex:: Вритексмлфиле</span><span class="sxs-lookup"><span data-stu-id="490ba-103">IXml2Dex::WriteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="490ba-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="490ba-104">\[Deprecated.</span></span> <span data-ttu-id="490ba-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="490ba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="490ba-106">`WriteXMLFile`Метод преобразует временную шкалу в XML и записывает XML-данные в файл.</span><span class="sxs-lookup"><span data-stu-id="490ba-106">The `WriteXMLFile` method translates a timeline to XML and writes the XML data to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="490ba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="490ba-107">Syntax</span></span>


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="490ba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="490ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="490ba-109">*птимелине*</span><span class="sxs-lookup"><span data-stu-id="490ba-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="490ba-110">Указатель на интерфейс **IUnknown** объекта временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="490ba-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="490ba-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="490ba-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="490ba-112">Строка, указывающая имя файла для записи.</span><span class="sxs-lookup"><span data-stu-id="490ba-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="490ba-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="490ba-113">Return value</span></span>

<span data-ttu-id="490ba-114">Возвращает значение **HRESULT** , которое зависит от реализации интерфейса.</span><span class="sxs-lookup"><span data-stu-id="490ba-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="490ba-115">**HRESULT** может включать одну из следующих стандартных констант или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="490ba-115">The **HRESULT** can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="490ba-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="490ba-116">Return code</span></span>                                                                                   | <span data-ttu-id="490ba-117">Описание</span><span class="sxs-lookup"><span data-stu-id="490ba-117">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="490ba-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="490ba-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="490ba-119">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="490ba-119">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="490ba-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="490ba-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="490ba-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="490ba-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="490ba-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="490ba-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="490ba-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="490ba-123">Success.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="490ba-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="490ba-124">Remarks</span></span>

<span data-ttu-id="490ba-125">Этот метод создает XML-файл, который представляет все компоненты на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="490ba-125">This method generates an XML file that represents all the components in the timeline.</span></span>

> [!Note]  
> <span data-ttu-id="490ba-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="490ba-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="490ba-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="490ba-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="490ba-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="490ba-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="490ba-129">Требования</span><span class="sxs-lookup"><span data-stu-id="490ba-129">Requirements</span></span>



| <span data-ttu-id="490ba-130">Требование</span><span class="sxs-lookup"><span data-stu-id="490ba-130">Requirement</span></span> | <span data-ttu-id="490ba-131">Значение</span><span class="sxs-lookup"><span data-stu-id="490ba-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="490ba-132">Версия</span><span class="sxs-lookup"><span data-stu-id="490ba-132">Version</span></span><br/> | <span data-ttu-id="490ba-133">Internet Explorer 4,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="490ba-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="490ba-134">Header</span><span class="sxs-lookup"><span data-stu-id="490ba-134">Header</span></span><br/>  | <dl> <span data-ttu-id="490ba-135"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="490ba-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="490ba-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="490ba-136">Library</span></span><br/> | <dl> <span data-ttu-id="490ba-137"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="490ba-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="490ba-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="490ba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490ba-139">**Интерфейс IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="490ba-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="490ba-140">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="490ba-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




