---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Логбуфферс'
title: Инстанцепараметерс. Логбуфферс, свойство
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702813"
---
# <a name="instanceparameterslogbuffers-property"></a><span data-ttu-id="ca104-103">Инстанцепараметерс. Логбуфферс, свойство</span><span class="sxs-lookup"><span data-stu-id="ca104-103">InstanceParameters.LogBuffers property</span></span>

<span data-ttu-id="ca104-104">Возвращает или задает объем памяти, используемый для кэширования записей журнала до их записи в файл журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="ca104-104">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="ca104-105">Единицей для этого параметра является размер сектора тома, содержащего файлы журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="ca104-105">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="ca104-106">Размер сектора почти всегда 512 байт, поэтому можно считать, что размер для единицы является надежным.</span><span class="sxs-lookup"><span data-stu-id="ca104-106">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="ca104-107">Этот параметр влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="ca104-107">This parameter has an impact on performance.</span></span> <span data-ttu-id="ca104-108">Когда ядро СУБД находится в режиме высокой нагрузки на обновление, этот буфер может быстро стать полностью загруженным.</span><span class="sxs-lookup"><span data-stu-id="ca104-108">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="ca104-109">Больший размер кэша для файла журнала транзакций очень важен для хорошего уровня производительности при такой высокой нагрузке.</span><span class="sxs-lookup"><span data-stu-id="ca104-109">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="ca104-110">Значение по умолчанию для этого случая известно слишком мало.</span><span class="sxs-lookup"><span data-stu-id="ca104-110">The default is known to be too small for this case.</span></span> <span data-ttu-id="ca104-111">Не устанавливайте для этого параметра количество буферов большего размера (в байтах), чем размер файла журнала транзакций, превышающий половину.</span><span class="sxs-lookup"><span data-stu-id="ca104-111">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<span data-ttu-id="ca104-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ca104-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ca104-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ca104-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ca104-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca104-114">Syntax</span></span>

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ca104-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ca104-115">Property value</span></span>

<span data-ttu-id="ca104-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ca104-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ca104-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca104-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ca104-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="ca104-118">Reference</span></span>

[<span data-ttu-id="ca104-119">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="ca104-119">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="ca104-120">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="ca104-120">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="ca104-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ca104-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
