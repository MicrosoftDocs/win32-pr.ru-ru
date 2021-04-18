---
description: Дополнительные сведения о методе API. Жетклосефилеинстанце
title: API. Жетклосефилеинстанце, метод
TOCTitle: 'JetCloseFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosefileinstance(v=EXCHG.10)
ms:contentKeyID: 55100663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ac29dec4032d83197a57746789afc770d84ec30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710853"
---
# <a name="apijetclosefileinstance-method"></a><span data-ttu-id="2539d-103">API. Жетклосефилеинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="2539d-103">Api.JetCloseFileInstance method</span></span>

<span data-ttu-id="2539d-104">Закрывает файл, Открытый с помощью Жетопенфилеинстанце после извлечения данных из этого файла с помощью Жетреадфилеинстанце.</span><span class="sxs-lookup"><span data-stu-id="2539d-104">Closes a file that was opened with JetOpenFileInstance after the data from that file has been extracted using JetReadFileInstance.</span></span>

<span data-ttu-id="2539d-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2539d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2539d-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2539d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2539d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2539d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseFileInstance ( _
    instance As JET_INSTANCE, _
    handle As JET_HANDLE _
)
'Usage
Dim instance As JET_INSTANCE
Dim handle As JET_HANDLEApi.JetCloseFileInstance(instance, _
    handle)
```

``` csharp
public static void JetCloseFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE handle
)
```

#### <a name="parameters"></a><span data-ttu-id="2539d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2539d-108">Parameters</span></span>

  - <span data-ttu-id="2539d-109">экземпляр</span><span class="sxs-lookup"><span data-stu-id="2539d-109">instance</span></span>  
    <span data-ttu-id="2539d-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2539d-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2539d-111">Используемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="2539d-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2539d-112">handle</span><span class="sxs-lookup"><span data-stu-id="2539d-112">handle</span></span>  
    <span data-ttu-id="2539d-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2539d-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="2539d-114">Закрывающий маркер.</span><span class="sxs-lookup"><span data-stu-id="2539d-114">The handle to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="2539d-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2539d-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2539d-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="2539d-116">Reference</span></span>

[<span data-ttu-id="2539d-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="2539d-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2539d-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="2539d-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2539d-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2539d-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
