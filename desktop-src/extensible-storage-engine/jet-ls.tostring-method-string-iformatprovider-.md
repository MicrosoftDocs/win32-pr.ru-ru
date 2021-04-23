---
description: 'Дополнительные сведения о: JET_LS. Метод ToString (String, IFormatProvider)'
title: JET_LS. Метод ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.tostring(v=EXCHG.10)
ms:contentKeyID: 39512228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9979a10ea3afe41a995661f1af8eac8cba80cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265543"
---
# <a name="jet_lstostring-method-string-iformatprovider"></a><span data-ttu-id="b2e20-103">JET_LS. Метод ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="b2e20-103">JET_LS.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="b2e20-104">Форматирует значение текущего экземпляра, используя указанный формат.</span><span class="sxs-lookup"><span data-stu-id="b2e20-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="b2e20-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2e20-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b2e20-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2e20-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e20-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2e20-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_LS
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

#### <a name="parameters"></a><span data-ttu-id="b2e20-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2e20-108">Parameters</span></span>

  - <span data-ttu-id="b2e20-109">format</span><span class="sxs-lookup"><span data-stu-id="b2e20-109">format</span></span>  
    <span data-ttu-id="b2e20-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b2e20-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b2e20-111">[Строка](/dotnet/api/system.string) , указывающая используемый формат.</span><span class="sxs-lookup"><span data-stu-id="b2e20-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="b2e20-112">-или-null, чтобы использовать формат по умолчанию, определенный для типа реализации [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="b2e20-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2e20-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="b2e20-113">formatProvider</span></span>  
    <span data-ttu-id="b2e20-114">Тип: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="b2e20-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="b2e20-115">[IFormatProvider](/dotnet/api/system.iformatprovider) , используемый для форматирования значения.</span><span class="sxs-lookup"><span data-stu-id="b2e20-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="b2e20-116">-или-null для получения сведений о форматировании чисел из текущего параметра языкового стандарта операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b2e20-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b2e20-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2e20-117">Return value</span></span>

<span data-ttu-id="b2e20-118">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b2e20-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="b2e20-119">[Строка](/dotnet/api/system.string) , содержащая значение текущего экземпляра в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="b2e20-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="b2e20-120">Реализации</span><span class="sxs-lookup"><span data-stu-id="b2e20-120">Implements</span></span>

[<span data-ttu-id="b2e20-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="b2e20-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="b2e20-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2e20-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2e20-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="b2e20-123">Reference</span></span>

[<span data-ttu-id="b2e20-124">Структура JET_LS</span><span class="sxs-lookup"><span data-stu-id="b2e20-124">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="b2e20-125">Элементы JET_LS</span><span class="sxs-lookup"><span data-stu-id="b2e20-125">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="b2e20-126">Перегрузка ToString</span><span class="sxs-lookup"><span data-stu-id="b2e20-126">ToString overload</span></span>](./jet-ls.tostring-method2.md)

[<span data-ttu-id="b2e20-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b2e20-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
