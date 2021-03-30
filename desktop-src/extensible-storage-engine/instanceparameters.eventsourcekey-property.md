---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Евентсаурцекэй'
title: Инстанцепараметерс. Евентсаурцекэй, свойство
TOCTitle: 'EventSourceKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsourcekey(v=EXCHG.10)
ms:contentKeyID: 55107449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSourceKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d1dc80943095611737d0c9704bcc0e82ffee506f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991430"
---
# <a name="instanceparameterseventsourcekey-property"></a><span data-ttu-id="0c399-103">Инстанцепараметерс. Евентсаурцекэй, свойство</span><span class="sxs-lookup"><span data-stu-id="0c399-103">InstanceParameters.EventSourceKey property</span></span>

<span data-ttu-id="0c399-104">Возвращает или задает имя журнала событий, используемого ядром СУБД для сообщений журнала событий.</span><span class="sxs-lookup"><span data-stu-id="0c399-104">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="0c399-105">По умолчанию все сообщения журнала событий перемещаются в журнал событий приложений.</span><span class="sxs-lookup"><span data-stu-id="0c399-105">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="0c399-106">Если будет настроено имя раздела реестра для другого журнала событий, вместо этого будут отправлены сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="0c399-106">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<span data-ttu-id="0c399-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c399-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c399-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c399-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c399-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c399-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSourceKey As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSourceKey

instance.EventSourceKey = value
```

``` csharp
public string EventSourceKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0c399-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0c399-110">Property value</span></span>

<span data-ttu-id="0c399-111">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0c399-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c399-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c399-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c399-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="0c399-113">Reference</span></span>

[<span data-ttu-id="0c399-114">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="0c399-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="0c399-115">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="0c399-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="0c399-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0c399-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
