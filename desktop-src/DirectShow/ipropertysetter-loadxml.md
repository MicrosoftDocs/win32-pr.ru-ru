---
description: Метод LoadXML загружает данные свойств, выраженные в язык XML (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Метод Ипропертисеттер:: LoadXML (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675023"
---
# <a name="ipropertysetterloadxml-method"></a><span data-ttu-id="ccf89-103">Метод Ипропертисеттер:: LoadXML</span><span class="sxs-lookup"><span data-stu-id="ccf89-103">IPropertySetter::LoadXML method</span></span>

> [!Note]  
> <span data-ttu-id="ccf89-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ccf89-104">\[Deprecated.</span></span> <span data-ttu-id="ccf89-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ccf89-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ccf89-106">`LoadXML`Метод загружает данные свойств, выраженные в язык XML (XML).</span><span class="sxs-lookup"><span data-stu-id="ccf89-106">The `LoadXML` method loads property data expressed in Extensible Markup Language (XML).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf89-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccf89-107">Syntax</span></span>


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a><span data-ttu-id="ccf89-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccf89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf89-109">*PXML* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ccf89-109">*pxml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf89-110">Указатель на интерфейс **IUnknown** элемента XML, созданного средством синтаксического анализа Microsoft XML.</span><span class="sxs-lookup"><span data-stu-id="ccf89-110">Pointer to the **IUnknown** interface of an XML element created by the Microsoft XML parser.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf89-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccf89-111">Return value</span></span>

<span data-ttu-id="ccf89-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccf89-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ccf89-113">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="ccf89-113">Possible values include the following.</span></span>



| <span data-ttu-id="ccf89-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ccf89-114">Return code</span></span>                                                                                                  | <span data-ttu-id="ccf89-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ccf89-115">Description</span></span>                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="ccf89-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-116"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="ccf89-117">Нет данных свойства.</span><span class="sxs-lookup"><span data-stu-id="ccf89-117">No property data.</span></span><br/>    |
| <dl> <span data-ttu-id="ccf89-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="ccf89-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ccf89-119">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="ccf89-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                | <span data-ttu-id="ccf89-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ccf89-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="ccf89-122"><dt>**\_ \_ Недопустимый \_ Формат файла VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-122"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="ccf89-123">Недопустимый формат.</span><span class="sxs-lookup"><span data-stu-id="ccf89-123">Invalid format.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="ccf89-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccf89-124">Remarks</span></span>

<span data-ttu-id="ccf89-125">Как правило, приложениям не требуется использовать этот метод.</span><span class="sxs-lookup"><span data-stu-id="ccf89-125">Typically, applications will not need to use this method.</span></span> <span data-ttu-id="ccf89-126">Алгоритм DES использует его для внутренней загрузки свойств из файлов КСТЛ.</span><span class="sxs-lookup"><span data-stu-id="ccf89-126">DES uses it internally to load properties from XTL files.</span></span>

<span data-ttu-id="ccf89-127">Чтобы использовать этот метод, создайте объект **IXMLDocument** и используйте его для синтаксического анализа XML-файла.</span><span class="sxs-lookup"><span data-stu-id="ccf89-127">To use this method, create an **IXMLDocument** object and use it to parse an XML file.</span></span> <span data-ttu-id="ccf89-128">Затем используйте объект **IXMLDocument** для получения объектов **иксмлелемент** .</span><span class="sxs-lookup"><span data-stu-id="ccf89-128">Then use the **IXMLDocument** object to retrieve **IXMLElement** objects.</span></span> <span data-ttu-id="ccf89-129">Если у объекта есть свойства, можно передать указатель **иксмлелемент** в метод **LoadXml** .</span><span class="sxs-lookup"><span data-stu-id="ccf89-129">If the object has properties, you can pass the **IXMLElement** pointer to the **LoadXML** method.</span></span> <span data-ttu-id="ccf89-130">Метод загружает свойства в метод задания свойства.</span><span class="sxs-lookup"><span data-stu-id="ccf89-130">The method loads the properties into the property setter.</span></span>

> [!Note]  
> <span data-ttu-id="ccf89-131">Интерфейсы **IXMLDocument** и **Иксмлелемент** реализуются в службах Microsoft XML Core Services (MSXML) версии 1,0, но не реализованы в более поздних версиях MSXML.</span><span class="sxs-lookup"><span data-stu-id="ccf89-131">The **IXMLDocument** and **IXMLElement** interfaces are implemented in Microsoft XML Core Services (MSXML) version 1.0, but are not implemented in more recent versions of MSXML.</span></span>

 

> [!Note]  
> <span data-ttu-id="ccf89-132">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ccf89-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ccf89-133">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ccf89-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ccf89-134">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ccf89-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccf89-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ccf89-135">Requirements</span></span>



| <span data-ttu-id="ccf89-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ccf89-136">Requirement</span></span> | <span data-ttu-id="ccf89-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ccf89-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf89-138">Header</span><span class="sxs-lookup"><span data-stu-id="ccf89-138">Header</span></span><br/>  | <dl> <span data-ttu-id="ccf89-139"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ccf89-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ccf89-140">Library</span></span><br/> | <dl> <span data-ttu-id="ccf89-141"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccf89-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf89-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccf89-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf89-143">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="ccf89-143">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="ccf89-144">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ccf89-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




