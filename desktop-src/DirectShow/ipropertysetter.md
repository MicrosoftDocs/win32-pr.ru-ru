---
description: 'Интерфейс Ипропертисеттер задает свойства для влияния или перехода в службах редактирования DirectShow (DES). Чтобы использовать этот интерфейс, создайте экземпляр объекта метода задания свойств (CLSID \_ пропертисеттер) и свяжите его с результатом или переходом, вызвав метод иамтимелинеобж:: сетпропертисеттер. Дополнительные сведения см. в разделе Работа с эффектами и переходами. обычно приложению необходимо вызвать только метод Ипропертисеттер:: Клеарпропс, чтобы очистить существующие свойства, и метод Ипропертисеттер:: Аддпроп для добавления новых свойств. Другие методы этого интерфейса вызываются другими компонентами DES.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Интерфейс Ипропертисеттер (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675821"
---
# <a name="ipropertysetter-interface"></a><span data-ttu-id="82835-105">Интерфейс Ипропертисеттер</span><span class="sxs-lookup"><span data-stu-id="82835-105">IPropertySetter interface</span></span>

> [!Note]  
> <span data-ttu-id="82835-106">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="82835-106">\[Deprecated.</span></span> <span data-ttu-id="82835-107">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82835-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82835-108">`IPropertySetter`Интерфейс задает свойства влияния или перехода в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="82835-108">The `IPropertySetter` interface sets properties on an effect or transition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="82835-109">Чтобы использовать этот интерфейс, создайте экземпляр объекта метода задания свойств (CLSID \_ пропертисеттер) и свяжите его с результатом или переходом, вызвав метод [**иамтимелинеобж:: сетпропертисеттер**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="82835-109">To use this interface, create an instance of a property setter object (CLSID\_PropertySetter), and associate it with an effect or transition by calling the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span> <span data-ttu-id="82835-110">Дополнительные сведения см. в разделе [Работа с эффектами и переходами](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="82835-110">For more information, see [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

<span data-ttu-id="82835-111">Обычно приложению необходимо вызвать метод [**ипропертисеттер:: клеарпропс**](ipropertysetter-clearprops.md) , чтобы очистить существующие свойства, и метод [**Ипропертисеттер:: аддпроп**](ipropertysetter-addprop.md) для добавления новых свойств.</span><span class="sxs-lookup"><span data-stu-id="82835-111">Usually an application needs to call only the [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) method to clear existing properties, and the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method to add new properties.</span></span> <span data-ttu-id="82835-112">Другие методы этого интерфейса вызываются другими компонентами DES.</span><span class="sxs-lookup"><span data-stu-id="82835-112">The other methods on this interface are called by other DES components.</span></span>

## <a name="members"></a><span data-ttu-id="82835-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="82835-113">Members</span></span>

<span data-ttu-id="82835-114">Интерфейс **ипропертисеттер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="82835-114">The **IPropertySetter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="82835-115">**Ипропертисеттер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="82835-115">**IPropertySetter** also has these types of members:</span></span>

-   [<span data-ttu-id="82835-116">Методы</span><span class="sxs-lookup"><span data-stu-id="82835-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="82835-117">Методы</span><span class="sxs-lookup"><span data-stu-id="82835-117">Methods</span></span>

<span data-ttu-id="82835-118">Интерфейс **ипропертисеттер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="82835-118">The **IPropertySetter** interface has these methods.</span></span>



| <span data-ttu-id="82835-119">Метод</span><span class="sxs-lookup"><span data-stu-id="82835-119">Method</span></span>                                               | <span data-ttu-id="82835-120">Описание</span><span class="sxs-lookup"><span data-stu-id="82835-120">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82835-121">**аддпроп**</span><span class="sxs-lookup"><span data-stu-id="82835-121">**AddProp**</span></span>](ipropertysetter-addprop.md)           | <span data-ttu-id="82835-122">Добавляет свойство в метод задания свойства с массивом пар «время-значение», определяющим значение свойства за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="82835-122">Adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span><br/> |
| [<span data-ttu-id="82835-123">**клеарпропс**</span><span class="sxs-lookup"><span data-stu-id="82835-123">**ClearProps**</span></span>](ipropertysetter-clearprops.md)     | <span data-ttu-id="82835-124">Удаляет все данные свойств из метода задания свойств.</span><span class="sxs-lookup"><span data-stu-id="82835-124">Clears all property data from the property setter.</span></span><br/>                                                                                 |
| [<span data-ttu-id="82835-125">**клонепропс**</span><span class="sxs-lookup"><span data-stu-id="82835-125">**CloneProps**</span></span>](ipropertysetter-cloneprops.md)     | <span data-ttu-id="82835-126">Копирует набор свойств из этого метода задания свойств и добавляет их в новый метод задания свойств.</span><span class="sxs-lookup"><span data-stu-id="82835-126">Clones a set of properties from this property setter and adds them to a new property setter.</span></span><br/>                                       |
| [<span data-ttu-id="82835-127">**фрипропс**</span><span class="sxs-lookup"><span data-stu-id="82835-127">**FreeProps**</span></span>](ipropertysetter-freeprops.md)       | <span data-ttu-id="82835-128">Освобождает ресурсы, выделенные методом [**ипропертисеттер:: "PROPS**](ipropertysetter-getprops.md) ".</span><span class="sxs-lookup"><span data-stu-id="82835-128">Frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span><br/>                             |
| [<span data-ttu-id="82835-129">**Props**</span><span class="sxs-lookup"><span data-stu-id="82835-129">**GetProps**</span></span>](ipropertysetter-getprops.md)         | <span data-ttu-id="82835-130">Извлекает свойства, заданные для этого объекта, с соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="82835-130">Retrieves the properties set on this object, with their corresponding values.</span></span><br/>                                                      |
| [<span data-ttu-id="82835-131">**лоадфромблоб**</span><span class="sxs-lookup"><span data-stu-id="82835-131">**LoadFromBlob**</span></span>](ipropertysetter-loadfromblob.md) | <span data-ttu-id="82835-132">Загружает данные свойств из формата сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="82835-132">Loads property data from a persistence format.</span></span><br/>                                                                                     |
| [<span data-ttu-id="82835-133">**LoadXML**</span><span class="sxs-lookup"><span data-stu-id="82835-133">**LoadXML**</span></span>](ipropertysetter-loadxml.md)           | <span data-ttu-id="82835-134">Загружает данные свойства, выраженные в язык XML (XML).</span><span class="sxs-lookup"><span data-stu-id="82835-134">Loads property data expressed in Extensible Markup Language (XML).</span></span><br/>                                                                 |
| [<span data-ttu-id="82835-135">**принтксмл**</span><span class="sxs-lookup"><span data-stu-id="82835-135">**PrintXML**</span></span>](ipropertysetter-printxml.md)         | <span data-ttu-id="82835-136">Преобразует данные свойств в XML-строку.</span><span class="sxs-lookup"><span data-stu-id="82835-136">Converts property data into an XML string.</span></span><br/>                                                                                         |
| [<span data-ttu-id="82835-137">**саветоблоб**</span><span class="sxs-lookup"><span data-stu-id="82835-137">**SaveToBlob**</span></span>](ipropertysetter-savetoblob.md)     | <span data-ttu-id="82835-138">Сохраняет данные свойства в формате сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="82835-138">Saves the property data to a persistence format.</span></span><br/>                                                                                   |
| [<span data-ttu-id="82835-139">**сетпропс**</span><span class="sxs-lookup"><span data-stu-id="82835-139">**SetProps**</span></span>](ipropertysetter-setprops.md)         | <span data-ttu-id="82835-140">Задает для свойств целевого объекта соответствующее состояние в течение указанного времени.</span><span class="sxs-lookup"><span data-stu-id="82835-140">Sets the properties of the target object to the appropriate state for the specified time.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="82835-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82835-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="82835-142">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="82835-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="82835-143">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="82835-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="82835-144">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="82835-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82835-145">Требования</span><span class="sxs-lookup"><span data-stu-id="82835-145">Requirements</span></span>



| <span data-ttu-id="82835-146">Требование</span><span class="sxs-lookup"><span data-stu-id="82835-146">Requirement</span></span> | <span data-ttu-id="82835-147">Значение</span><span class="sxs-lookup"><span data-stu-id="82835-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82835-148">Header</span><span class="sxs-lookup"><span data-stu-id="82835-148">Header</span></span><br/>  | <dl> <span data-ttu-id="82835-149"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="82835-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="82835-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82835-150">Library</span></span><br/> | <dl> <span data-ttu-id="82835-151"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82835-151"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
