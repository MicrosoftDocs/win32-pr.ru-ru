---
description: Метод Реадксмлфиле загружает файл XML-проекта.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'Метод IXml2Dex:: Реадксмлфиле (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689338"
---
# <a name="ixml2dexreadxmlfile-method"></a><span data-ttu-id="9331b-103">Метод IXml2Dex:: Реадксмлфиле</span><span class="sxs-lookup"><span data-stu-id="9331b-103">IXml2Dex::ReadXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="9331b-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9331b-104">\[Deprecated.</span></span> <span data-ttu-id="9331b-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9331b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9331b-106">`ReadXMLFile`Метод загружает файл XML-проекта.</span><span class="sxs-lookup"><span data-stu-id="9331b-106">The `ReadXMLFile` method loads an XML project file.</span></span> <span data-ttu-id="9331b-107">Этот метод создает экземпляры всех объектов, выраженные в XML-файле и вставляет их на временную шкалу, а также применяет любые атрибуты, заданные для временной шкалы, такие как частота кадров или эффекты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9331b-107">This method creates instances of all the objects expressed in the XML file and inserts them into the timeline, as well as applying any attributes given for the timeline, such as frame rate or default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="9331b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9331b-108">Syntax</span></span>


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a><span data-ttu-id="9331b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9331b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9331b-110">*птимелине*</span><span class="sxs-lookup"><span data-stu-id="9331b-110">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="9331b-111">Указатель на интерфейс **IUnknown** объекта временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="9331b-111">Pointer to a timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="9331b-112">*XMLName*</span><span class="sxs-lookup"><span data-stu-id="9331b-112">*XMLName*</span></span> 
</dt> <dd>

<span data-ttu-id="9331b-113">Строка, указывающая имя загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="9331b-113">String that specifies the name of the file to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9331b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9331b-114">Return value</span></span>

<span data-ttu-id="9331b-115">Возвращает значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="9331b-115">Returns an HRESULT value.</span></span> <span data-ttu-id="9331b-116">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="9331b-116">Possible values include the following.</span></span>



| <span data-ttu-id="9331b-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9331b-117">Return code</span></span>                                                                                                  | <span data-ttu-id="9331b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9331b-118">Description</span></span>                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="9331b-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9331b-119"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="9331b-120">Успешно</span><span class="sxs-lookup"><span data-stu-id="9331b-120">Success</span></span><br/>             |
| <dl> <span data-ttu-id="9331b-121"><dt>**\_ \_ Недопустимый \_ Формат файла VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9331b-121"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="9331b-122">Недопустимый формат файла</span><span class="sxs-lookup"><span data-stu-id="9331b-122">Invalid file format</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9331b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9331b-123">Remarks</span></span>

<span data-ttu-id="9331b-124">Этот метод не удаляет существующие объекты с временной шкалы перед вставкой новых объектов, определенных в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="9331b-124">This method does not clear existing objects from the timeline before it inserts the new objects defined in the XML file.</span></span> <span data-ttu-id="9331b-125">Если необходимо обновить существующую временную шкалу, сначала вызовите метод [**иамтимелине:: клеараллграупс**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="9331b-125">If you need to refresh an existing timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) first.</span></span>

> [!Note]  
> <span data-ttu-id="9331b-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="9331b-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9331b-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9331b-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9331b-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9331b-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9331b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9331b-129">Requirements</span></span>



| <span data-ttu-id="9331b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9331b-130">Requirement</span></span> | <span data-ttu-id="9331b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9331b-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9331b-132">Версия</span><span class="sxs-lookup"><span data-stu-id="9331b-132">Version</span></span><br/> | <span data-ttu-id="9331b-133">Internet Explorer 4,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9331b-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="9331b-134">Header</span><span class="sxs-lookup"><span data-stu-id="9331b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9331b-135"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="9331b-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9331b-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9331b-136">Library</span></span><br/> | <dl> <span data-ttu-id="9331b-137"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9331b-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9331b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9331b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9331b-139">**Интерфейс IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="9331b-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="9331b-140">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="9331b-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




