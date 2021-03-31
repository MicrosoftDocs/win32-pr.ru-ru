---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Клеанупмисматчедлогфилес'
title: Инстанцепараметерс. Клеанупмисматчедлогфилес, свойство
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155403"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a><span data-ttu-id="07eba-103">Инстанцепараметерс. Клеанупмисматчедлогфилес, свойство</span><span class="sxs-lookup"><span data-stu-id="07eba-103">InstanceParameters.CleanupMismatchedLogFiles property</span></span>

<span data-ttu-id="07eba-104">Возвращает или задает значение, указывающее, завершается ли Жетинит сбоем, когда ядро СУБД настроено для начала использования файлов журнала транзакций на диске, размер которых отличается от настроенного.</span><span class="sxs-lookup"><span data-stu-id="07eba-104">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="07eba-105">Обычно [жетинит (JET_INSTANCE)](./api.jetinit-method.md) успешно восстановит базы данных, но завершится с ошибкой [логфилесиземисматчдатабасесконсистент](./jet-err-enumeration.md) , чтобы указать, что размер файла журнала настроен неправильно.</span><span class="sxs-lookup"><span data-stu-id="07eba-105">Normally, [JetInit(JET_INSTANCE)](./api.jetinit-method.md) will successfully recover the databases but will fail with [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="07eba-106">Однако если этот параметр имеет значение true, то ядро СУБД автоматически удалит все старые файлы журналов, а затем запустит новый набор файлов журнала транзакций, используя настроенный размер файла журнала.</span><span class="sxs-lookup"><span data-stu-id="07eba-106">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="07eba-107">Этот параметр полезен, когда приложению требуется прозрачно изменить размер файла журнала транзакций, но все равно работать прозрачно в сценариях обновления и восстановления.</span><span class="sxs-lookup"><span data-stu-id="07eba-107">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<span data-ttu-id="07eba-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07eba-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07eba-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07eba-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07eba-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07eba-110">Syntax</span></span>

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="07eba-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="07eba-111">Property value</span></span>

<span data-ttu-id="07eba-112">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="07eba-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="07eba-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07eba-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07eba-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="07eba-114">Reference</span></span>

[<span data-ttu-id="07eba-115">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="07eba-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="07eba-116">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="07eba-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="07eba-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="07eba-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
