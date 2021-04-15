---
description: 'Дополнительные сведения о методе: Циммофдесериализер. Десериализеклассес (Byte [], UInt32, IEnumerable <CimClass> , String, String, онкласснидед, жетинклудедфилеконтент)'
title: Метод Циммофдесериализер. Десериализеклассес (Byte [], UInt32, IEnumerable (Цимкласс), строка, строка, Онкласснидед, Жетинклудедфилеконтент) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},System.String,System.String,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 5772ca08a94c27e1ae0b110e05192004b9e4df2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539770"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-string-string-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="f2471-103">Циммофдесериализер. Десериализеклассес, метод (Byte \[ \] , UInt32, IEnumerable \<CimClass\> , строка, строка, онкласснидед, жетинклудедфилеконтент)</span><span class="sxs-lookup"><span data-stu-id="f2471-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>, String, String, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="f2471-104">Десериализует классы CIM на основе сериализованных данных, коллекции родительских классов CIM, имен компьютеров и пространств имен и обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="f2471-104">Deserializes CIM classes based on serialized data, collection of parent CIM classes, computer and namespace names, and callbacks.</span></span>

<span data-ttu-id="f2471-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2471-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="f2471-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="f2471-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="f2471-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2471-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    string computerName,
    string namespaceName,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    String^ computerName,
    String^ namespaceName,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        computerName:string *
        namespaceName:string *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    computerName As String,
    namespaceName As String,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="f2471-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2471-108">Parameters</span></span>

  - <span data-ttu-id="f2471-109">сериализеддата</span><span class="sxs-lookup"><span data-stu-id="f2471-109">serializedData</span></span>  
    <span data-ttu-id="f2471-110">Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="f2471-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="f2471-111">Буфер, содержащий сериализованные данные.</span><span class="sxs-lookup"><span data-stu-id="f2471-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2471-112">offset</span><span class="sxs-lookup"><span data-stu-id="f2471-112">offset</span></span>  
    <span data-ttu-id="f2471-113">Тип: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="f2471-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="f2471-114">Смещение в байтах к расположению, с которого начинается чтение данных.</span><span class="sxs-lookup"><span data-stu-id="f2471-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="f2471-115">Когда метод возвращает значение, смещение будет указывать на следующий байт после десериализованных классов.</span><span class="sxs-lookup"><span data-stu-id="f2471-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2471-116">-классы;</span><span class="sxs-lookup"><span data-stu-id="f2471-116">classes</span></span>  
    <span data-ttu-id="f2471-117">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f2471-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="f2471-118">Необязательный кэш родительских классов CIM.</span><span class="sxs-lookup"><span data-stu-id="f2471-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2471-119">computerName</span><span class="sxs-lookup"><span data-stu-id="f2471-119">computerName</span></span>  
    [<span data-ttu-id="f2471-120">System.String</span><span class="sxs-lookup"><span data-stu-id="f2471-120">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="f2471-121">имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="f2471-121">The computer name.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2471-122">namespaceName</span><span class="sxs-lookup"><span data-stu-id="f2471-122">namespaceName</span></span>  
    [<span data-ttu-id="f2471-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f2471-123">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="f2471-124">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f2471-124">The namespace name.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2471-125">онкласснидедкаллбакк</span><span class="sxs-lookup"><span data-stu-id="f2471-125">onClassNeededCallback</span></span>  
    <span data-ttu-id="f2471-126">Тип: [онкласснидед](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="f2471-126">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="f2471-127">Функция обратного вызова, используемая для предоставления запрошенного объекта класса во время десериализации.</span><span class="sxs-lookup"><span data-stu-id="f2471-127">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2471-128">жетинклудедфилекаллбакк</span><span class="sxs-lookup"><span data-stu-id="f2471-128">getIncludedFileCallback</span></span>  
    <span data-ttu-id="f2471-129">Тип: [жетинклудедфилеконтент](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="f2471-129">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="f2471-130">Функция обратного вызова, используемая для предоставления содержимого буфера файла указанного файла.</span><span class="sxs-lookup"><span data-stu-id="f2471-130">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f2471-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2471-131">Return value</span></span>

<span data-ttu-id="f2471-132">Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f2471-132">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="f2471-133">Интерфейс [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) , который может использоваться для перечисления классов CIM.</span><span class="sxs-lookup"><span data-stu-id="f2471-133">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2471-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2471-134">See also</span></span>

<span data-ttu-id="f2471-135">[Класс Цимкласс](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2471-135">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="f2471-136">[Пространство имен Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2471-136">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
