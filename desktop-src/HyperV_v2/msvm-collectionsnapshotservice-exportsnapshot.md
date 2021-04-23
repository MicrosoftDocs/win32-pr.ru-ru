---
description: Экспортирует коллекцию моментальных снимков для систем виртуальных компьютеров в файл. Коллекция моментальных снимков, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Метод Експортснапшот класса Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263856"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="c1aa5-104">Метод Експортснапшот \_ класса Коллектионснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="c1aa5-104">ExportSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="c1aa5-105">Экспортирует коллекцию моментальных снимков для систем виртуальных компьютеров в файл.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-105">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="c1aa5-106">Коллекция моментальных снимков, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-106">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1aa5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1aa5-107">Syntax</span></span>


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c1aa5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1aa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1aa5-109">*Снапшотколлектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1aa5-109">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aa5-110">Ссылка на [**\_ коллекцию CIM**](cim-collection.md) , которая представляет коллекцию моментальных снимков для экспорта.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="c1aa5-111">*Експортдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1aa5-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aa5-112">Полный путь к каталогу, в который должна быть экспортирована коллекция виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-112">The fully-qualified path of the directory to which the virtual system collection is to be exported.</span></span> <span data-ttu-id="c1aa5-113">Если свойство **креатевмекспортсубдиректори** в параметре *Експортсеттингдата* имеет значение **true** , этот каталог можно использовать повторно для экспорта нескольких коллекций виртуальных систем, и этот метод помещает каждое определение коллекции виртуальных систем в отдельный подкаталог под этим путем.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-113">If the **CreateVmExportSubdirectory** property in the *ExportSettingData* parameter is set to **True** then this directory can be reused for exporting multiple virtual system collections and this method places each virtual system collection definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="c1aa5-114">*Експортсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1aa5-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aa5-115">Экземпляр [**мсвм \_ коллектионснапшотекспортсеттингдата**](msvm-collectionsnapshotexportsettingdata.md) , представляющий параметры для операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-115">An instance of [**Msvm\_CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1aa5-116">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c1aa5-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aa5-117">Необязательная ссылка, которая возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-117">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="c1aa5-118">При наличии возвращаемой ссылки на экземпляр [**CIM \_ конкретежоб**](cim-concretejob.md) можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-118">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1aa5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1aa5-119">Return value</span></span>

<span data-ttu-id="c1aa5-120">Если этот метод выполняется синхронно, он возвращает 0, если он выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-120">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="c1aa5-121">Если этот метод выполняется асинхронно, возвращается 4096, а для отслеживания хода выполнения асинхронной операции можно использовать выходной параметр задания.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-121">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="c1aa5-122">Любое другое возвращаемое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c1aa5-122">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1aa5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c1aa5-123">Requirements</span></span>



| <span data-ttu-id="c1aa5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c1aa5-124">Requirement</span></span> | <span data-ttu-id="c1aa5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c1aa5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1aa5-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1aa5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c1aa5-127">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c1aa5-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c1aa5-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1aa5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c1aa5-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c1aa5-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c1aa5-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1aa5-130">Namespace</span></span><br/>                | <span data-ttu-id="c1aa5-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c1aa5-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c1aa5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c1aa5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1aa5-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa5-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1aa5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c1aa5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1aa5-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa5-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1aa5-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1aa5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1aa5-137">**Мсвм \_ коллектионснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="c1aa5-137">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




