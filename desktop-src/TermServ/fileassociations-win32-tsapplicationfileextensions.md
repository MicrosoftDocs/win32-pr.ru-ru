---
title: Метод ФилеассоЦиатионс класса Win32_TSApplicationFileExtensions
description: Сканирует реестр для получения текущих сопоставлений файлов для приложения.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ФилеассоЦиатионс
- Службы удаленных рабочих столов метода ФилеассоЦиатионс, класс Win32_TSApplicationFileExtensions
- Класс Win32_TSApplicationFileExtensions службы удаленных рабочих столов, метод ФилеассоЦиатионс
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682088"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="cca0c-106">Метод ФилеассоЦиатионс \_ класса Win32 тсаппликатионфиликстенсионс</span><span class="sxs-lookup"><span data-stu-id="cca0c-106">FileAssociations method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="cca0c-107">Сканирует реестр для получения текущих сопоставлений файлов для приложения.</span><span class="sxs-lookup"><span data-stu-id="cca0c-107">Scans the registry to get the current file associations for an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca0c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cca0c-108">Syntax</span></span>


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a><span data-ttu-id="cca0c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cca0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca0c-110">*Апппас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cca0c-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cca0c-111">Указывает путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="cca0c-111">Specifies the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="cca0c-112">*ФилеассоЦиатионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cca0c-112">*FileAssociations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cca0c-113">При успешном завершении содержит сопоставления файлов для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="cca0c-113">On successful completion contains the file associations for this application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cca0c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cca0c-114">Requirements</span></span>



| <span data-ttu-id="cca0c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cca0c-115">Requirement</span></span> | <span data-ttu-id="cca0c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cca0c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cca0c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cca0c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cca0c-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cca0c-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cca0c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cca0c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cca0c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cca0c-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="cca0c-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cca0c-121">Namespace</span></span><br/>                | <span data-ttu-id="cca0c-122">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="cca0c-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cca0c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="cca0c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cca0c-124"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cca0c-124"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="cca0c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cca0c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cca0c-126"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cca0c-126"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca0c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cca0c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca0c-128">**\_Тсаппликатионфиликстенсионс Win32**</span><span class="sxs-lookup"><span data-stu-id="cca0c-128">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> <dt>

[<span data-ttu-id="cca0c-129">**\_РдфилеассоЦиатион Win32**</span><span class="sxs-lookup"><span data-stu-id="cca0c-129">**Win32\_RDFileAssociation**</span></span>](win32-rdfileassociation.md)
</dt> </dl>

 

 





