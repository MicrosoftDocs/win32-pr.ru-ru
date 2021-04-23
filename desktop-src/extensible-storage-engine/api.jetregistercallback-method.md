---
description: Дополнительные сведения о методе API. Жетрегистеркаллбакк
title: API. Жетрегистеркаллбакк, метод
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703157"
---
# <a name="apijetregistercallback-method"></a><span data-ttu-id="609fd-103">API. Жетрегистеркаллбакк, метод</span><span class="sxs-lookup"><span data-stu-id="609fd-103">Api.JetRegisterCallback method</span></span>

<span data-ttu-id="609fd-104">Позволяет приложению настроить ядро СУБД на выдачу уведомлений для конкретных событий в приложении.</span><span class="sxs-lookup"><span data-stu-id="609fd-104">Allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="609fd-105">Эти уведомления связаны с определенной таблицей и остаются в силе только до тех пор, пока экземпляр, содержащий таблицу, не завершит работу с помощью [жеттерм (JET_INSTANCE)](./api.jetterm-method.md).</span><span class="sxs-lookup"><span data-stu-id="609fd-105">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm(JET_INSTANCE)](./api.jetterm-method.md).</span></span>

<span data-ttu-id="609fd-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="609fd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="609fd-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="609fd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="609fd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="609fd-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="609fd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="609fd-109">Parameters</span></span>

  - <span data-ttu-id="609fd-110">сесид</span><span class="sxs-lookup"><span data-stu-id="609fd-110">sesid</span></span>  
    <span data-ttu-id="609fd-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="609fd-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="609fd-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="609fd-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="609fd-113">TableID</span><span class="sxs-lookup"><span data-stu-id="609fd-113">tableid</span></span>  
    <span data-ttu-id="609fd-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="609fd-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="609fd-115">Курсор, Открытый в таблице, в которой должен быть зарегистрирован обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="609fd-115">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="609fd-116">кбтип</span><span class="sxs-lookup"><span data-stu-id="609fd-116">cbtyp</span></span>  
    <span data-ttu-id="609fd-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="609fd-117">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="609fd-118">Причины обратного вызова, для которых приложение хочет получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="609fd-118">The callback reasons for which the application wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="609fd-119">обратный вызов</span><span class="sxs-lookup"><span data-stu-id="609fd-119">callback</span></span>  
    <span data-ttu-id="609fd-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="609fd-120">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="609fd-121">Функция обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="609fd-121">The callback function.</span></span>

<!-- end list -->

  - <span data-ttu-id="609fd-122">контекст</span><span class="sxs-lookup"><span data-stu-id="609fd-122">context</span></span>  
    <span data-ttu-id="609fd-123">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="609fd-123">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="609fd-124">Контекст, который будет передан обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="609fd-124">A context that will be given to the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="609fd-125">каллбаккид</span><span class="sxs-lookup"><span data-stu-id="609fd-125">callbackId</span></span>  
    <span data-ttu-id="609fd-126">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="609fd-126">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="609fd-127">Маркер, который впоследствии можно использовать для отмены регистрации заданной функции обратного вызова с помощью [жетунрегистеркаллбакк (JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span><span class="sxs-lookup"><span data-stu-id="609fd-127">A handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="609fd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="609fd-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="609fd-129">Справочник</span><span class="sxs-lookup"><span data-stu-id="609fd-129">Reference</span></span>

[<span data-ttu-id="609fd-130">Класс API</span><span class="sxs-lookup"><span data-stu-id="609fd-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="609fd-131">Члены API</span><span class="sxs-lookup"><span data-stu-id="609fd-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="609fd-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="609fd-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
