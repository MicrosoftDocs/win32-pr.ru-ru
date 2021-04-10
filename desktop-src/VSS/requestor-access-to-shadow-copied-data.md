---
description: После завершения теневой копии наиболее важный механизм получения доступа к содержащимся в нем данным файлов заключается в использовании объекта устройства теневой копии.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Доступ инициатора запроса к теневым скопированным данным
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156111"
---
# <a name="requester-access-to-shadow-copied-data"></a><span data-ttu-id="d126c-103">Доступ инициатора запроса к теневым скопированным данным</span><span class="sxs-lookup"><span data-stu-id="d126c-103">Requester Access to Shadow Copied Data</span></span>

<span data-ttu-id="d126c-104">После завершения теневой копии наиболее важный механизм получения доступа к содержащимся в нем данным файлов заключается в использовании [*объекта устройства*](vssgloss-d.md)теневой копии.</span><span class="sxs-lookup"><span data-stu-id="d126c-104">Once the shadow copy has completed, the most important mechanism for getting access to the file data it contains is through the use of the shadow copy's [*device object*](vssgloss-d.md).</span></span>

<span data-ttu-id="d126c-105">Элемент **m \_ пвсзснапшотдевицеобжект** структуры [**\_ снимков \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) представляет собой строку, содержащую объект устройства теневого копирования тома.</span><span class="sxs-lookup"><span data-stu-id="d126c-105">The **m\_pwszSnapshotDeviceObject** member of a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure is a string containing a shadow-copied volume's device object.</span></span> <span data-ttu-id="d126c-106">Инициатор запроса может получить объект **\_ \_ prop snapshot** теневого копирования тома VSS, если он знает **\_ идентификатор VSS** тома (идентифицирует идентификатор GUID) и передает его в [**ивссбаккупкомпонентс:: жетснапшотпропертиес**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="d126c-106">A requester can obtain a shadow-copied volume's **VSS\_SNAPSHOT\_PROP** object if it knows the volume's **VSS\_ID** (identifying GUID) and passes it to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="d126c-107">Инициатор запроса может также получить сведения о свойстве теневого копирования с помощью элемента **obj. Snap** структуры [**\_ объекта \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (структура snapshot, которая представляет собой структуру [**\_ снимков \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ), полученную с помощью [**ивссенумобжект**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) , чтобы выполнить итерацию по списку объектов, возвращенных вызовом [**ивссбаккупкомпонентс:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="d126c-107">A requester can also obtain shadow copy property information by using the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) structure (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

<span data-ttu-id="d126c-108">Объект устройства должен интерпретироваться как корень тома, скопированного с помощью теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="d126c-108">The device object should be interpreted as the root of a shadow-copied volume.</span></span> <span data-ttu-id="d126c-109">По этой причине объект устройства не содержит обратную косую черту (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="d126c-109">For this reason, the device object contains no backslash ("\\").</span></span>

<span data-ttu-id="d126c-110">Пути к теневому скопированному тому получаются путем замены корня исходного пути на объект устройства.</span><span class="sxs-lookup"><span data-stu-id="d126c-110">Paths on the shadow copied volume are obtained by replacing the root of the original path with the device object.</span></span> <span data-ttu-id="d126c-111">Например, по указанному пути к исходному тому "C: \\ Database \\ \* . mdb" и экземпляру [**снаппроп \_ снимка \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) можно получить путь к теневому скопированному тому путем сцепления снаппропм \_ пвсзшадов копидевицеобжект, " \\ " и " \\ Database \\ \* . mdb".</span><span class="sxs-lookup"><span data-stu-id="d126c-111">For example, given a path on the original volume of "C:\\DATABASE\\\*.mdb" and a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) instance of snapProp, you would obtain the path on the shadow copied volume by concatenating snapPropm\_pwszShadow copyDeviceObject, "\\", and "\\DATABASE\\\*.mdb".</span></span>

<span data-ttu-id="d126c-112">Наборы файлов VSS могут содержать подстановочные знаки в дескрипторах файлов, поэтому получение полного списка файлов в теневой копии, управляемой компонентом, может потребовать использования таких методов, как **финдфилефирст**, **финдфилефирстекс** и **FindNextFile**.</span><span class="sxs-lookup"><span data-stu-id="d126c-112">The VSS file sets might have wildcard characters in their file descriptors, so obtaining a full list of the files on a shadow copy managed by a component might require the use of methods such as **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>

 

 



