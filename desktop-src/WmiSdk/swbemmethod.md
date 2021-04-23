---
description: Можно использовать свойства объекта Свбеммесод для проверки одного определения метода объекта WMI. Не удается создать этот объект с помощью вызова функции VBScript.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Объект Свбеммесод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544674"
---
# <a name="swbemmethod-object"></a><span data-ttu-id="a4a35-104">Объект Свбеммесод</span><span class="sxs-lookup"><span data-stu-id="a4a35-104">SWbemMethod object</span></span>

<span data-ttu-id="a4a35-105">Можно использовать свойства объекта **свбеммесод** для проверки одного определения метода объекта WMI.</span><span class="sxs-lookup"><span data-stu-id="a4a35-105">You can use the properties of the **SWbemMethod** object to inspect a single method definition of a WMI object.</span></span> <span data-ttu-id="a4a35-106">Не удается создать этот объект с **помощью вызова функции** VBScript.</span><span class="sxs-lookup"><span data-stu-id="a4a35-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="a4a35-107">Этот объект можно использовать для проверки определений методов.</span><span class="sxs-lookup"><span data-stu-id="a4a35-107">This object can be used to inspect the definitions of methods.</span></span> <span data-ttu-id="a4a35-108">Для вызова методов следует использовать либо прямой доступ (см. раздел [Управление информацией о классах и экземплярах](manipulating-class-and-instance-information.md)) на [**SWbemObject**](swbemobject.md) (который является рекомендуемым механизмом), либо вызовом [**кмесодSWbemServices.Exe**](swbemservices-execmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a35-108">To invoke the methods, you should use either direct access (see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md)) on an [**SWbemObject**](swbemobject.md) (which is the recommended mechanism) object, or the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span>

> [!Note]  
> <span data-ttu-id="a4a35-109">В этой версии API доступ на запись к сведениям о методе не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a4a35-109">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="a4a35-110">Если необходимо определить методы или изменить существующие определения методов, можно определить изменения метода в MOF-файле и отправить изменения с помощью [компилятора MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="a4a35-110">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the [MOF Compiler](compiling-mof-files.md).</span></span> <span data-ttu-id="a4a35-111">Кроме того, можно использовать [API COM для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a4a35-111">Alternatively, use the [COM API for WMI](com-api-for-wmi.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="a4a35-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="a4a35-112">Members</span></span>

<span data-ttu-id="a4a35-113">Объект **свбеммесод** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a4a35-113">The **SWbemMethod** object has these types of members:</span></span>

-   [<span data-ttu-id="a4a35-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4a35-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4a35-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4a35-115">Properties</span></span>

<span data-ttu-id="a4a35-116">Объект **свбеммесод** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a4a35-116">The **SWbemMethod** object has these properties.</span></span>



| <span data-ttu-id="a4a35-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="a4a35-117">Property</span></span>                                                      | <span data-ttu-id="a4a35-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="a4a35-118">Access type</span></span>          | <span data-ttu-id="a4a35-119">Описание</span><span class="sxs-lookup"><span data-stu-id="a4a35-119">Description</span></span>                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4a35-120">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="a4a35-120">**InParameters**</span></span>](swbemmethod-inparameters.md)<br/>   | <span data-ttu-id="a4a35-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4a35-121">Read-only</span></span><br/> | <span data-ttu-id="a4a35-122">Объект [**SWbemObject**](swbemobject.md) , свойства которого определяют входные параметры для этого метода.</span><span class="sxs-lookup"><span data-stu-id="a4a35-122">An [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span><br/>              |
| [<span data-ttu-id="a4a35-123">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a4a35-123">**Name**</span></span>](swbemmethod-name.md)<br/>                   | <span data-ttu-id="a4a35-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4a35-124">Read-only</span></span><br/> | <span data-ttu-id="a4a35-125">Имя метода.</span><span class="sxs-lookup"><span data-stu-id="a4a35-125">Name of the method.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="a4a35-126">**Лета**</span><span class="sxs-lookup"><span data-stu-id="a4a35-126">**Origin**</span></span>](swbemmethod-origin.md)<br/>               | <span data-ttu-id="a4a35-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4a35-127">Read-only</span></span><br/> | <span data-ttu-id="a4a35-128">Исходный класс метода.</span><span class="sxs-lookup"><span data-stu-id="a4a35-128">Originating class of the method.</span></span><br/>                                                                                        |
| [<span data-ttu-id="a4a35-129">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="a4a35-129">**OutParameters**</span></span>](swbemmethod-outparameters.md)<br/> | <span data-ttu-id="a4a35-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4a35-130">Read-only</span></span><br/> | <span data-ttu-id="a4a35-131">Объект [**SWbemObject**](swbemobject.md) , свойства которого определяют выходные параметры и тип возвращаемого значения этого метода.</span><span class="sxs-lookup"><span data-stu-id="a4a35-131">An [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span><br/> |
| [<span data-ttu-id="a4a35-132">**Квалификаторы\_**</span><span class="sxs-lookup"><span data-stu-id="a4a35-132">**Qualifiers\_**</span></span>](swbemmethod-qualifiers-.md)<br/>    | <span data-ttu-id="a4a35-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4a35-133">Read-only</span></span><br/> | <span data-ttu-id="a4a35-134">Объект [**свбемкуалифиерсет**](swbemqualifierset.md) , содержащий квалификаторы для данного метода.</span><span class="sxs-lookup"><span data-stu-id="a4a35-134">An [**SWbemQualifierSet**](swbemqualifierset.md) object that contains the qualifiers for this method.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="a4a35-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a4a35-135">Requirements</span></span>



| <span data-ttu-id="a4a35-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a4a35-136">Requirement</span></span> | <span data-ttu-id="a4a35-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a4a35-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a35-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4a35-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a35-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4a35-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4a35-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4a35-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a35-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4a35-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4a35-142">Header</span><span class="sxs-lookup"><span data-stu-id="a4a35-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4a35-143"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4a35-143"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4a35-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a4a35-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4a35-145"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4a35-145"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4a35-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a35-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4a35-147"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4a35-147"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4a35-148">CLSID</span><span class="sxs-lookup"><span data-stu-id="a4a35-148">CLSID</span></span><br/>                    | <span data-ttu-id="a4a35-149">\_СВБЕММЕСОД CLSID</span><span class="sxs-lookup"><span data-stu-id="a4a35-149">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="a4a35-150">IID</span><span class="sxs-lookup"><span data-stu-id="a4a35-150">IID</span></span><br/>                      | <span data-ttu-id="a4a35-151">IID \_ исвбеммесод</span><span class="sxs-lookup"><span data-stu-id="a4a35-151">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="a4a35-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4a35-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a35-153">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="a4a35-153">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




