---
description: Квалификатор Цимтипе содержит текст, описывающий тип свойства.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Квалификатор Цимтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156830"
---
# <a name="cimtype-qualifier"></a><span data-ttu-id="a97c7-103">Квалификатор Цимтипе</span><span class="sxs-lookup"><span data-stu-id="a97c7-103">CIMType Qualifier</span></span>

<span data-ttu-id="a97c7-104">Квалификатор **Цимтипе** содержит текст, описывающий тип свойства.</span><span class="sxs-lookup"><span data-stu-id="a97c7-104">The **CIMType** qualifier contains text describing the type of a property.</span></span>

<span data-ttu-id="a97c7-105">Этот текст может представлять собой MOF-тип, например "String" и "Sint32", или тип CIM, например "CIM \_ String" и "CIM \_ Sint32".</span><span class="sxs-lookup"><span data-stu-id="a97c7-105">This text can be the MOF type such as "string" and "sint32" or the CIM type such as "CIM\_STRING" and "CIM\_SINT32".</span></span> <span data-ttu-id="a97c7-106">Между квалификатором **Цимтипе** и типом свойства, используемым в параметре *пвттипе* метода [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) , существует соответствие "один к одному".</span><span class="sxs-lookup"><span data-stu-id="a97c7-106">There is a one-to-one correspondence between the **CIMType** qualifier and the type of the property used in the *pvtType* parameter of the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="a97c7-107">Это два исключения:</span><span class="sxs-lookup"><span data-stu-id="a97c7-107">The two exceptions are:</span></span>

-   <span data-ttu-id="a97c7-108">[*Свойства ссылки*](gloss-r.md), имеющие **\_ ссылку на тип CIM**, которая содержит значение "ref: ClassName".</span><span class="sxs-lookup"><span data-stu-id="a97c7-108">[*Reference properties*](gloss-r.md), which have the type **CIM\_REFERENCE**, that contains the "REF:classname" value.</span></span> <span data-ttu-id="a97c7-109">Значение ClassName описывает тип класса ссылочного свойства.</span><span class="sxs-lookup"><span data-stu-id="a97c7-109">The classname value describes the class type of the reference property.</span></span>
-   <span data-ttu-id="a97c7-110">Свойства внедренного объекта, имеющие тип **\_ объекта CIM** .</span><span class="sxs-lookup"><span data-stu-id="a97c7-110">Embedded object properties, which have the **CIM\_OBJECT** type.</span></span>

<span data-ttu-id="a97c7-111">Однако обратите внимание, что квалификатор **Цимтипе** может и должен использоваться для более точного ввода ссылочного свойства.</span><span class="sxs-lookup"><span data-stu-id="a97c7-111">Please note, however, that the **CIMType** qualifier can and should be used to type a reference property more exactly.</span></span> <span data-ttu-id="a97c7-112">Например, если свойство всегда ссылается на экземпляры класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , его квалификатор **Цимтипе** должен иметь значение:</span><span class="sxs-lookup"><span data-stu-id="a97c7-112">For example, if the property always refers to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class, its **CIMType** qualifier should be set to:</span></span>


```mof
"ref:Win32_LogicalDisk"
```



<span data-ttu-id="a97c7-113">По умолчанию квалификатор **Цимтипе** ссылочного свойства имеет тип **ref**.</span><span class="sxs-lookup"><span data-stu-id="a97c7-113">By default, the **CIMType** qualifier of a reference property has the type **ref**.</span></span>

<span data-ttu-id="a97c7-114">Как и в случае со свойствами ссылки, квалификатор **Цимтипе** должен использоваться для ввода свойства внедренного объекта более точно с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="a97c7-114">As with reference properties, the **CIMType** qualifier should used to type an embedded object property more exactly with the following syntax:</span></span>


```mof
"object:EmbedClass"
```



<span data-ttu-id="a97c7-115">Поскольку Инструментарий WMI поддерживает больше типов, чем могут быть выражены стандартными константами с помощью \_ префикса VT, квалификатор **Цимтипе** может помочь интерпретировать значения типа.</span><span class="sxs-lookup"><span data-stu-id="a97c7-115">Because WMI allows more types than can be expressed by standard constants with the VT\_ prefix, the **CIMType** qualifier can help interpret type values.</span></span> <span data-ttu-id="a97c7-116">Квалификатор **Цимтипе** добавляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="a97c7-116">The **CIMType** qualifier is added automatically.</span></span> <span data-ttu-id="a97c7-117">Дополнительные сведения см. в разделе [типы данных MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="a97c7-117">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a97c7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a97c7-118">Requirements</span></span>



| <span data-ttu-id="a97c7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a97c7-119">Requirement</span></span> | <span data-ttu-id="a97c7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a97c7-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a97c7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a97c7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a97c7-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a97c7-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a97c7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a97c7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a97c7-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a97c7-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a97c7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a97c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97c7-126">**Стандартные квалификаторы WMI**</span><span class="sxs-lookup"><span data-stu-id="a97c7-126">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="a97c7-127">Квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="a97c7-127">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="a97c7-128">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="a97c7-128">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

