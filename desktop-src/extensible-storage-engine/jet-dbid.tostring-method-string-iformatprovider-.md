---
description: 'Дополнительные сведения о: JET_DBID. Метод ToString (String, IFormatProvider)'
title: JET_DBID. Метод ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513106
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f9c950c86e4f749c7889fcf6914b8294850f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682684"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a><span data-ttu-id="4f178-103">JET_DBID. Метод ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="4f178-103">JET_DBID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="4f178-104">Форматирует значение текущего экземпляра, используя указанный формат.</span><span class="sxs-lookup"><span data-stu-id="4f178-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="4f178-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4f178-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4f178-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4f178-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f178-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f178-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_DBID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a><span data-ttu-id="4f178-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f178-108">Parameters</span></span>

  - <span data-ttu-id="4f178-109">format</span><span class="sxs-lookup"><span data-stu-id="4f178-109">format</span></span>  
    <span data-ttu-id="4f178-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4f178-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4f178-111">[Строка](/dotnet/api/system.string) , указывающая используемый формат.</span><span class="sxs-lookup"><span data-stu-id="4f178-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="4f178-112">-или-null, чтобы использовать формат по умолчанию, определенный для типа реализации [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="4f178-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f178-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="4f178-113">formatProvider</span></span>  
    <span data-ttu-id="4f178-114">Тип: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="4f178-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="4f178-115">[IFormatProvider](/dotnet/api/system.iformatprovider) , используемый для форматирования значения.</span><span class="sxs-lookup"><span data-stu-id="4f178-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="4f178-116">-или-null для получения сведений о форматировании чисел из текущего параметра языкового стандарта операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4f178-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4f178-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f178-117">Return value</span></span>

<span data-ttu-id="4f178-118">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4f178-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="4f178-119">[Строка](/dotnet/api/system.string) , содержащая значение текущего экземпляра в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="4f178-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="4f178-120">Реализации</span><span class="sxs-lookup"><span data-stu-id="4f178-120">Implements</span></span>

[<span data-ttu-id="4f178-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="4f178-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="4f178-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f178-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4f178-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="4f178-123">Reference</span></span>

[<span data-ttu-id="4f178-124">Структура JET_DBID</span><span class="sxs-lookup"><span data-stu-id="4f178-124">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="4f178-125">Элементы JET_DBID</span><span class="sxs-lookup"><span data-stu-id="4f178-125">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="4f178-126">Перегрузка ToString</span><span class="sxs-lookup"><span data-stu-id="4f178-126">ToString overload</span></span>](./jet-dbid.tostring-method.md)

[<span data-ttu-id="4f178-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4f178-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
