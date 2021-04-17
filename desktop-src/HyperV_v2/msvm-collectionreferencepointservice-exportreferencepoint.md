---
description: Экспортирует коллекцию опорных точек в файл. Коллекция опорных точек, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Метод Експортреференцепоинт класса Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684623"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="6a2e5-104">Метод Експортреференцепоинт \_ класса Коллектионреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6a2e5-104">ExportReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="6a2e5-105">Экспортирует коллекцию опорных точек в файл.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-105">Exports a reference point collection to a file.</span></span> <span data-ttu-id="6a2e5-106">Коллекция опорных точек, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-106">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a2e5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a2e5-107">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6a2e5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a2e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a2e5-109">*Референцепоинтколлектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-109">*ReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-110">Ссылка на [**\_ коллекцию CIM**](cim-collection.md) , представляющую коллекцию точек ссылки для экспорта.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the reference point collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-111">*Експортдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-112">Полный путь к каталогу, в который должна быть экспортирована коллекция опорных точек.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-112">The fully-qualified path of the directory to which the reference point collection is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-113">*Експортсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-113">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-114">Экземпляр [**мсвм \_ коллектионреференцепоинтекспортсеттингдата**](msvm-collectionreferencepointexportsettingdata.md) , представляющий параметры для операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-114">An instance of [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-115">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-116">Необязательная ссылка, которая возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-116">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="6a2e5-117">При наличии возвращаемой ссылки на экземпляр [**CIM \_ конкретежоб**](cim-concretejob.md) можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-117">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a2e5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a2e5-118">Return value</span></span>

<span data-ttu-id="6a2e5-119">Если этот метод выполняется синхронно, он возвращает 0, если он выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-119">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="6a2e5-120">Если этот метод выполняется асинхронно, возвращается 4096, а для отслеживания хода выполнения асинхронной операции можно использовать выходной параметр задания.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-120">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="6a2e5-121">Любое другое возвращаемое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-121">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a2e5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6a2e5-122">Requirements</span></span>



| <span data-ttu-id="6a2e5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6a2e5-123">Requirement</span></span> | <span data-ttu-id="6a2e5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6a2e5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a2e5-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a2e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6a2e5-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6a2e5-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a2e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6a2e5-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6a2e5-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6a2e5-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6a2e5-129">Namespace</span></span><br/>                | <span data-ttu-id="6a2e5-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6a2e5-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a2e5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6a2e5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a2e5-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a2e5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a2e5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6a2e5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a2e5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a2e5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a2e5-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a2e5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a2e5-136">**Мсвм \_ коллектионреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="6a2e5-136">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




