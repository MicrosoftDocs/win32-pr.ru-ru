---
description: 'Дополнительные сведения о: Циммофдесериализер. Жетинклудедфилеконтент Delegate (строка)'
title: Циммофдесериализер. Жетинклудедфилеконтент-делегат (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.GetIncludedFileContent delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::GetIncludedFileContent
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: cb922d785da7d01de93adec56cefee29785210d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719413"
---
# <a name="cimmofdeserializergetincludedfilecontent-delegate-string"></a><span data-ttu-id="6db82-103">Циммофдесериализер. Жетинклудедфилеконтент-делегат (String)</span><span class="sxs-lookup"><span data-stu-id="6db82-103">CimMofDeserializer.GetIncludedFileContent delegate (String)</span></span>

<span data-ttu-id="6db82-104">Представляет обратный вызов для получения содержимого файла в виде массива байтов.</span><span class="sxs-lookup"><span data-stu-id="6db82-104">Represents a callback to retrieve the file's contents in the form of a byte array.</span></span>

<span data-ttu-id="6db82-105">**Пространство имен:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6db82-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="6db82-106">**Сборка:**  Microsoft. Management. Infrastructure (в Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="6db82-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="6db82-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6db82-107">Syntax</span></span>

``` csharp
public delegate byte[] GetIncludedFileContent(
    string fileName
)
```

``` c++
public delegate array<unsigned char>^ GetIncludedFileContent(
    String^ fileName
)
```

``` fsharp
type GetIncludedFileContent = 
    delegate of 
        fileName:string -> byte[]
```

``` vb
Public Delegate Function GetIncludedFileContent (
    fileName As String
) As Byte()
```

#### <a name="parameters"></a><span data-ttu-id="6db82-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6db82-108">Parameters</span></span>

  - <span data-ttu-id="6db82-109">fileName</span><span class="sxs-lookup"><span data-stu-id="6db82-109">fileName</span></span>  
    <span data-ttu-id="6db82-110">Тип: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="6db82-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="6db82-111">Имя файла, включая путь.</span><span class="sxs-lookup"><span data-stu-id="6db82-111">File name, including path.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6db82-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6db82-112">Return Value</span></span>

<span data-ttu-id="6db82-113">Тип: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="6db82-113">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>

<span data-ttu-id="6db82-114">Возвращает содержимое файла в виде массива байтов.</span><span class="sxs-lookup"><span data-stu-id="6db82-114">Returns the file's contents in the form of a byte array.</span></span>

## <a name="see-also"></a><span data-ttu-id="6db82-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="6db82-115">See Also</span></span>

<span data-ttu-id="6db82-116">[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6db82-116">[Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
