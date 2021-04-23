---
description: 'Дополнительные сведения о: JET_INSTANCE. Метод ToString (String, IFormatProvider)'
title: JET_INSTANCE. Метод ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.tostring(v=EXCHG.10)
ms:contentKeyID: 39511283
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4030a86ed867a2463346dca549acb35809264c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656647"
---
# <a name="jet_instancetostring-method-string-iformatprovider"></a><span data-ttu-id="eb625-103">JET_INSTANCE. Метод ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="eb625-103">JET_INSTANCE.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="eb625-104">Форматирует значение текущего экземпляра, используя указанный формат.</span><span class="sxs-lookup"><span data-stu-id="eb625-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="eb625-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb625-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb625-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb625-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb625-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb625-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_INSTANCE
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

#### <a name="parameters"></a><span data-ttu-id="eb625-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb625-108">Parameters</span></span>

  - <span data-ttu-id="eb625-109">format</span><span class="sxs-lookup"><span data-stu-id="eb625-109">format</span></span>  
    <span data-ttu-id="eb625-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="eb625-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="eb625-111">[Строка](/dotnet/api/system.string) , указывающая используемый формат. или значение null, чтобы использовать формат по умолчанию, определенный для типа реализации [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="eb625-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb625-112">formatProvider</span><span class="sxs-lookup"><span data-stu-id="eb625-112">formatProvider</span></span>  
    <span data-ttu-id="eb625-113">Тип: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="eb625-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="eb625-114">[IFormatProvider](/dotnet/api/system.iformatprovider) , используемый для форматирования значения; или значение NULL для получения сведений о форматировании чисел из текущего параметра языкового стандарта операционной системы.</span><span class="sxs-lookup"><span data-stu-id="eb625-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="eb625-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb625-115">Return value</span></span>

<span data-ttu-id="eb625-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="eb625-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="eb625-117">[Строка](/dotnet/api/system.string) , содержащая значение текущего экземпляра в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="eb625-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="eb625-118">Реализации</span><span class="sxs-lookup"><span data-stu-id="eb625-118">Implements</span></span>

[<span data-ttu-id="eb625-119">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="eb625-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="eb625-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb625-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb625-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="eb625-121">Reference</span></span>

[<span data-ttu-id="eb625-122">Структура JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="eb625-122">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="eb625-123">Элементы JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="eb625-123">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="eb625-124">Перегрузка ToString</span><span class="sxs-lookup"><span data-stu-id="eb625-124">ToString overload</span></span>](./jet-instance.tostring-method2.md)

[<span data-ttu-id="eb625-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="eb625-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
