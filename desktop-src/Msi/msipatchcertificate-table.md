---
description: Определяет возможные сертификаты подписи, используемые для цифровых подписей.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Таблица Мсипатчцертификате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080916"
---
# <a name="msipatchcertificate-table"></a><span data-ttu-id="3a3ee-103">Таблица Мсипатчцертификате</span><span class="sxs-lookup"><span data-stu-id="3a3ee-103">MsiPatchCertificate Table</span></span>

<span data-ttu-id="3a3ee-104">В таблице Мсипатчцертификате указаны возможные сертификаты для подписи, используемые для цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-104">The MsiPatchCertificate Table identifies the possible signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="3a3ee-105">Таблица Мсипатчцертификате содержит сведения, необходимые для включения [исправления контроля учетных записей пользователей (UAC)](user-account-control--uac--patching.md) для приложения.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-105">The MsiPatchCertificate Table contains the information that is needed to enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for an application.</span></span>

<span data-ttu-id="3a3ee-106">Таблица Мсипатчцертификате содержит следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="3a3ee-106">The MsiPatchCertificate Table has the following columns:</span></span>



| <span data-ttu-id="3a3ee-107">Столбец</span><span class="sxs-lookup"><span data-stu-id="3a3ee-107">Column</span></span>               | <span data-ttu-id="3a3ee-108">Type</span><span class="sxs-lookup"><span data-stu-id="3a3ee-108">Type</span></span>                         | <span data-ttu-id="3a3ee-109">Ключ</span><span class="sxs-lookup"><span data-stu-id="3a3ee-109">Key</span></span> | <span data-ttu-id="3a3ee-110">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="3a3ee-110">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="3a3ee-111">патчцертификате</span><span class="sxs-lookup"><span data-stu-id="3a3ee-111">PatchCertificate</span></span>     | [<span data-ttu-id="3a3ee-112">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="3a3ee-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="3a3ee-113">Да</span><span class="sxs-lookup"><span data-stu-id="3a3ee-113">Y</span></span>   | <span data-ttu-id="3a3ee-114">Нет</span><span class="sxs-lookup"><span data-stu-id="3a3ee-114">N</span></span>        |
| <span data-ttu-id="3a3ee-115">дигиталцертификате\_</span><span class="sxs-lookup"><span data-stu-id="3a3ee-115">DigitalCertificate\_</span></span> | [<span data-ttu-id="3a3ee-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="3a3ee-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="3a3ee-117">Нет</span><span class="sxs-lookup"><span data-stu-id="3a3ee-117">N</span></span>   | <span data-ttu-id="3a3ee-118">Нет</span><span class="sxs-lookup"><span data-stu-id="3a3ee-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3a3ee-119">Столбцы</span><span class="sxs-lookup"><span data-stu-id="3a3ee-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3a3ee-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>патчцертификате</span><span class="sxs-lookup"><span data-stu-id="3a3ee-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span></span>
</dt> <dd>

<span data-ttu-id="3a3ee-121">Уникальный идентификатор этой строки в таблице Мсипатчцертификате.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-121">The unique identifier for this row in the MsiPatchCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="3a3ee-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>дигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="3a3ee-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="3a3ee-123">Внешний ключ в первом столбце [таблицы мсидигиталцертификате](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="3a3ee-123">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="3a3ee-124">Строка, указанная в таблице Мсидигиталцертификате, содержит двоичное представление сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-124">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a3ee-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a3ee-125">Remarks</span></span>

<span data-ttu-id="3a3ee-126">Исправления всегда оцениваются по таблице Мсипатчцертификате, которая является текущей на момент применения исправления.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-126">Patches are always evaluated against the MsiPatchCertificate Table that is current at the time the patch is applied.</span></span> <span data-ttu-id="3a3ee-127">Исправление может изменить таблицу Мсипатчцертификате, добавляя или удаляя записи.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-127">A patch can modify the MsiPatchCertificate Table by adding or removing entries.</span></span> <span data-ttu-id="3a3ee-128">Это позволяет исправить оценку будущих исправлений, которые будут применены позже в последовательности исправлений.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-128">This enables a patch to modify the evaluation of future patches that are applied later in the patching sequence.</span></span> <span data-ttu-id="3a3ee-129">В таблице может быть несколько сертификатов, и исправление должно соответствовать по крайней мере одному сертификату, который должен быть применен.</span><span class="sxs-lookup"><span data-stu-id="3a3ee-129">Multiple certificates can exist in the table, and the patch must match at least one certificate to be applied.</span></span>

## <a name="validation"></a><span data-ttu-id="3a3ee-130">Проверка</span><span class="sxs-lookup"><span data-stu-id="3a3ee-130">Validation</span></span>

<dl>

[<span data-ttu-id="3a3ee-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="3a3ee-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3a3ee-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="3a3ee-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3a3ee-133">ICE32</span><span class="sxs-lookup"><span data-stu-id="3a3ee-133">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3a3ee-134">ICE81</span><span class="sxs-lookup"><span data-stu-id="3a3ee-134">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="3a3ee-135">См. также</span><span class="sxs-lookup"><span data-stu-id="3a3ee-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a3ee-136">дисаблелуапатчинг</span><span class="sxs-lookup"><span data-stu-id="3a3ee-136">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="3a3ee-137">Исправление контроля учетных записей пользователей (UAC)</span><span class="sxs-lookup"><span data-stu-id="3a3ee-137">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="3a3ee-138">**мсидисаблелуапатчинг**</span><span class="sxs-lookup"><span data-stu-id="3a3ee-138">**MSIDISABLELUAPATCHING**</span></span>](msidisableluapatching.md)
</dt> <dt>

[<span data-ttu-id="3a3ee-139">Цифровые подписи и установщик Windows</span><span class="sxs-lookup"><span data-stu-id="3a3ee-139">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="3a3ee-140">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="3a3ee-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



