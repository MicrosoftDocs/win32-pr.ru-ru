---
description: 'Дополнительные сведения: метод API. Жетжетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: Метод API. Жетжетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100727
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 840c17ef1d74b57b4bee75b9efafe5a314f09a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896997"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a><span data-ttu-id="1f1ae-103">Метод API. Жетжетсистемпараметер (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-103">Api.JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span></span>

<span data-ttu-id="1f1ae-104">Возвращает параметры конфигурации базы данных.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-104">Gets database configuration options.</span></span>

<span data-ttu-id="1f1ae-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f1ae-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f1ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f1ae-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As Integer, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref int paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a><span data-ttu-id="1f1ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f1ae-108">Parameters</span></span>

  - <span data-ttu-id="1f1ae-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="1f1ae-109">instance</span></span>  
    <span data-ttu-id="1f1ae-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="1f1ae-111">Экземпляр, из которого извлекаются параметры.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-111">The instance to retrieve the options from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f1ae-112">сесид</span><span class="sxs-lookup"><span data-stu-id="1f1ae-112">sesid</span></span>  
    <span data-ttu-id="1f1ae-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1f1ae-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f1ae-115">paramid</span><span class="sxs-lookup"><span data-stu-id="1f1ae-115">paramid</span></span>  
    <span data-ttu-id="1f1ae-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="1f1ae-117">Получаемый параметр.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-117">The parameter to get.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f1ae-118">paramValue</span><span class="sxs-lookup"><span data-stu-id="1f1ae-118">paramValue</span></span>  
    <span data-ttu-id="1f1ae-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1f1ae-120">Возвращает значение параметра, если значение является целым числом.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-120">Returns the value of the parameter, if the value is an integer.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f1ae-121">парамстринг</span><span class="sxs-lookup"><span data-stu-id="1f1ae-121">paramString</span></span>  
    <span data-ttu-id="1f1ae-122">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1f1ae-123">Возвращает значение параметра, если значение является строкой.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-123">Returns the value of the parameter, if the value is a string.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f1ae-124">макспарам</span><span class="sxs-lookup"><span data-stu-id="1f1ae-124">maxParam</span></span>  
    <span data-ttu-id="1f1ae-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1f1ae-126">Максимальный размер строки параметра.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-126">The maximum size of the parameter string.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1f1ae-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f1ae-127">Return value</span></span>

<span data-ttu-id="1f1ae-128">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-128">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="1f1ae-129">Код предупреждения ESENT.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-129">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="1f1ae-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f1ae-130">Remarks</span></span>

<span data-ttu-id="1f1ae-131">[Еррортостринг](./jet-param-enumeration.md) передает номер ошибки в paramValue, поэтому он является параметром ref, а не параметром out.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-131">[ErrorToString](./jet-param-enumeration.md) passes in the error number in the paramValue, which is why it is a ref parameter and not an out parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f1ae-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f1ae-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f1ae-133">Справочник</span><span class="sxs-lookup"><span data-stu-id="1f1ae-133">Reference</span></span>

[<span data-ttu-id="1f1ae-134">Класс API</span><span class="sxs-lookup"><span data-stu-id="1f1ae-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1f1ae-135">Члены API</span><span class="sxs-lookup"><span data-stu-id="1f1ae-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1f1ae-136">Перегрузка Жетжетсистемпараметер</span><span class="sxs-lookup"><span data-stu-id="1f1ae-136">JetGetSystemParameter overload</span></span>](./api.jetgetsystemparameter-method.md)

[<span data-ttu-id="1f1ae-137">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1f1ae-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
