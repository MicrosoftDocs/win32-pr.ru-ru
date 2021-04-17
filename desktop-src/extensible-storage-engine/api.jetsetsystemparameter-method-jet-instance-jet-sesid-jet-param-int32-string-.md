---
description: 'Дополнительные сведения: метод API. Жетсетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String)'
title: Метод API. Жетсетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100811
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd320c42e1d24c0919010706ae3f7e61a65b78a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703308"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string"></a><span data-ttu-id="92e5f-103">Метод API. Жетсетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</span><span class="sxs-lookup"><span data-stu-id="92e5f-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</span></span>

<span data-ttu-id="92e5f-104">Задает параметры конфигурации базы данных.</span><span class="sxs-lookup"><span data-stu-id="92e5f-104">Sets database configuration options.</span></span>

<span data-ttu-id="92e5f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92e5f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92e5f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="92e5f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92e5f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92e5f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As Integer, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    int paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="92e5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92e5f-108">Parameters</span></span>

  - <span data-ttu-id="92e5f-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="92e5f-109">instance</span></span>  
    <span data-ttu-id="92e5f-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92e5f-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="92e5f-111">Экземпляр, устанавливающий параметр ON или [nil](./jet-instance.nil-property.md) , чтобы задать параметр для всех экземпляров.</span><span class="sxs-lookup"><span data-stu-id="92e5f-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="92e5f-112">сесид</span><span class="sxs-lookup"><span data-stu-id="92e5f-112">sesid</span></span>  
    <span data-ttu-id="92e5f-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92e5f-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="92e5f-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="92e5f-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="92e5f-115">paramid</span><span class="sxs-lookup"><span data-stu-id="92e5f-115">paramid</span></span>  
    <span data-ttu-id="92e5f-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="92e5f-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="92e5f-117">Заданный параметр.</span><span class="sxs-lookup"><span data-stu-id="92e5f-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="92e5f-118">paramValue</span><span class="sxs-lookup"><span data-stu-id="92e5f-118">paramValue</span></span>  
    <span data-ttu-id="92e5f-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="92e5f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="92e5f-120">Значение параметра, которое необходимо задать, если параметр имеет целочисленный тип.</span><span class="sxs-lookup"><span data-stu-id="92e5f-120">The value of the parameter to set, if the parameter is an integer type.</span></span>

<!-- end list -->

  - <span data-ttu-id="92e5f-121">парамстринг</span><span class="sxs-lookup"><span data-stu-id="92e5f-121">paramString</span></span>  
    <span data-ttu-id="92e5f-122">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="92e5f-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="92e5f-123">Значение параметра, которое необходимо задать, если параметр имеет строковый тип.</span><span class="sxs-lookup"><span data-stu-id="92e5f-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="92e5f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92e5f-124">Return value</span></span>

<span data-ttu-id="92e5f-125">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="92e5f-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="92e5f-126">Код предупреждения ESENT.</span><span class="sxs-lookup"><span data-stu-id="92e5f-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="92e5f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92e5f-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92e5f-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="92e5f-128">Reference</span></span>

[<span data-ttu-id="92e5f-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="92e5f-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="92e5f-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="92e5f-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="92e5f-131">Перегрузка Жетсетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="92e5f-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="92e5f-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="92e5f-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
