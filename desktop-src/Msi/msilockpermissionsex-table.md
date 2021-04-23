---
description: Таблицу Мсилоккпермиссионсекс можно использовать для защиты служб, файлов, разделов реестра и созданных папок.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Таблица Мсилоккпермиссионсекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674219"
---
# <a name="msilockpermissionsex-table"></a><span data-ttu-id="7bfba-103">Таблица Мсилоккпермиссионсекс</span><span class="sxs-lookup"><span data-stu-id="7bfba-103">MsiLockPermissionsEx Table</span></span>

<span data-ttu-id="7bfba-104">Таблицу Мсилоккпермиссионсекс можно использовать для защиты служб, файлов, разделов реестра и созданных папок.</span><span class="sxs-lookup"><span data-stu-id="7bfba-104">The MsiLockPermissionsEx Table can be used to secure services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="7bfba-105">Пакет не должен содержать как таблицу Мсилоккпермиссионсекс, так и [таблицу локкпермиссионс](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="7bfba-105">A package should not contain both the MsiLockPermissionsEx Table and the [LockPermissions Table](lockpermissions-table.md).</span></span>

<span data-ttu-id="7bfba-106">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7bfba-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="7bfba-107">Эта таблица рекомендуется для пакетов, предназначенных для установки с установщик Windows 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7bfba-107">This table is recommended for packages intended for installation with Windows Installer 5.0 or later.</span></span>

<span data-ttu-id="7bfba-108">Таблица Мсилоккпермиссионсекс содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="7bfba-108">The MsiLockPermissionsEx Table has the following columns.</span></span>



| <span data-ttu-id="7bfba-109">Столбец</span><span class="sxs-lookup"><span data-stu-id="7bfba-109">Column</span></span>               | <span data-ttu-id="7bfba-110">Type</span><span class="sxs-lookup"><span data-stu-id="7bfba-110">Type</span></span>                                       | <span data-ttu-id="7bfba-111">Ключ</span><span class="sxs-lookup"><span data-stu-id="7bfba-111">Key</span></span> | <span data-ttu-id="7bfba-112">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="7bfba-112">Nullable</span></span> |
|----------------------|--------------------------------------------|-----|----------|
| <span data-ttu-id="7bfba-113">мсилоккпермиссионсекс</span><span class="sxs-lookup"><span data-stu-id="7bfba-113">MsiLockPermissionsEx</span></span> | [<span data-ttu-id="7bfba-114">Text</span><span class="sxs-lookup"><span data-stu-id="7bfba-114">Text</span></span>](text.md)                           | <span data-ttu-id="7bfba-115">Да</span><span class="sxs-lookup"><span data-stu-id="7bfba-115">Y</span></span>   | <span data-ttu-id="7bfba-116">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-116">N</span></span>        |
| <span data-ttu-id="7bfba-117">LockObject</span><span class="sxs-lookup"><span data-stu-id="7bfba-117">LockObject</span></span>           | [<span data-ttu-id="7bfba-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7bfba-118">Identifier</span></span>](identifier.md)               | <span data-ttu-id="7bfba-119">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-119">N</span></span>   | <span data-ttu-id="7bfba-120">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-120">N</span></span>        |
| <span data-ttu-id="7bfba-121">Таблица</span><span class="sxs-lookup"><span data-stu-id="7bfba-121">Table</span></span>                | [<span data-ttu-id="7bfba-122">Text</span><span class="sxs-lookup"><span data-stu-id="7bfba-122">Text</span></span>](text.md)                           | <span data-ttu-id="7bfba-123">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-123">N</span></span>   | <span data-ttu-id="7bfba-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-124">N</span></span>        |
| <span data-ttu-id="7bfba-125">сддлтекст</span><span class="sxs-lookup"><span data-stu-id="7bfba-125">SDDLText</span></span>             | [<span data-ttu-id="7bfba-126">форматтедсддлтекст</span><span class="sxs-lookup"><span data-stu-id="7bfba-126">FormattedSDDLText</span></span>](formattedsddltext.md) | <span data-ttu-id="7bfba-127">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-127">N</span></span>   | <span data-ttu-id="7bfba-128">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-128">N</span></span>        |
| <span data-ttu-id="7bfba-129">Условие</span><span class="sxs-lookup"><span data-stu-id="7bfba-129">Condition</span></span>            | [<span data-ttu-id="7bfba-130">Condition</span><span class="sxs-lookup"><span data-stu-id="7bfba-130">Condition</span></span>](condition.md)                 | <span data-ttu-id="7bfba-131">Нет</span><span class="sxs-lookup"><span data-stu-id="7bfba-131">N</span></span>   | <span data-ttu-id="7bfba-132">Да</span><span class="sxs-lookup"><span data-stu-id="7bfba-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7bfba-133">Столбцы</span><span class="sxs-lookup"><span data-stu-id="7bfba-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7bfba-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>мсилоккпермиссионсекс</span><span class="sxs-lookup"><span data-stu-id="7bfba-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span></span>
</dt> <dd>

<span data-ttu-id="7bfba-135">Это первичный ключ этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="7bfba-135">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="7bfba-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="7bfba-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="7bfba-137">Этот столбец и столбец таблицы вместе указывают файл, каталог, раздел реестра или службу, которая должна быть защищена.</span><span class="sxs-lookup"><span data-stu-id="7bfba-137">This column and the Table column together specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="7bfba-138">Столбец LockObject — это внешний ключ, указывающий на первичный ключ таблицы, заданный столбцом таблицы.</span><span class="sxs-lookup"><span data-stu-id="7bfba-138">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="7bfba-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="7bfba-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="7bfba-140">В этом столбце и столбце LockObject указывается файл, каталог, раздел реестра или служба, которая должна быть защищена.</span><span class="sxs-lookup"><span data-stu-id="7bfba-140">This column and the LockObject column specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="7bfba-141">В столбце Таблица введите file, Registry, Креатефолдер или Сервицеинсталл, чтобы указать LockObject, перечисленные в [таблице файлов](file-table.md), [таблице реестра](registry-table.md), [таблице креатефолдер](createfolder-table.md)или [таблице сервицеинсталл](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="7bfba-141">In the Table column, enter File, Registry, CreateFolder, or ServiceInstall to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), [CreateFolder Table](createfolder-table.md), or [ServiceInstall Table](serviceinstall-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bfba-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>сддлтекст</span><span class="sxs-lookup"><span data-stu-id="7bfba-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span></span>
</dt> <dd>

<span data-ttu-id="7bfba-143">Введите строку SDDL, чтобы указать разрешения, применяемые к выбранному объекту.</span><span class="sxs-lookup"><span data-stu-id="7bfba-143">Enter the SDDL string to indicate permissions to apply to selected object.</span></span> <span data-ttu-id="7bfba-144">В [формате строки дескриптора безопасности](../secauthz/security-descriptor-string-format.md)должен быть указан SDDL.</span><span class="sxs-lookup"><span data-stu-id="7bfba-144">The SDDL must be provided in [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span>

<span data-ttu-id="7bfba-145">Это не поддерживает закрытые или открытые свойства.</span><span class="sxs-lookup"><span data-stu-id="7bfba-145">This does not support private or public properties.</span></span>

</dd> <dt>

<span data-ttu-id="7bfba-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="7bfba-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="7bfba-147">Этот столбец содержит условное выражение, используемое для определения того, следует ли применять указанное разрешение.</span><span class="sxs-lookup"><span data-stu-id="7bfba-147">This column contains a conditional expression used to determine whether to apply the specified permission.</span></span> <span data-ttu-id="7bfba-148">Если условие принимает **значение false**, то разрешение не применяется.</span><span class="sxs-lookup"><span data-stu-id="7bfba-148">If the condition evaluates to **FALSE**, the permission is not applied.</span></span> <span data-ttu-id="7bfba-149">Если условие принимает **значение true**, применяется разрешение.</span><span class="sxs-lookup"><span data-stu-id="7bfba-149">If the condition evaluates to **TRUE**, the permission is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bfba-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bfba-150">Remarks</span></span>

<span data-ttu-id="7bfba-151">Дополнительные сведения о защите служб, файлов, разделов реестра и созданных папок см. в статье [Защита ресурсов](securing-resources-.md).</span><span class="sxs-lookup"><span data-stu-id="7bfba-151">See [Securing Resources](securing-resources-.md)for more information about securing services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="7bfba-152">Используйте таблицу Мсилоккпермиссионсекс для защиты объектов учетной записи пользователя, создаваемой во время установки.</span><span class="sxs-lookup"><span data-stu-id="7bfba-152">Use the MsiLockPermissionsEx Table to secure objects for a user account that is being created during the installation.</span></span> <span data-ttu-id="7bfba-153">Учетная запись пользователя должна уже существовать, когда установка защищает объект.</span><span class="sxs-lookup"><span data-stu-id="7bfba-153">The user account must already exist when the installation secures the object.</span></span> <span data-ttu-id="7bfba-154">Создайте учетную запись пользователя перед установкой файла, раздела реестра, папки или службы, которые будут защищены.</span><span class="sxs-lookup"><span data-stu-id="7bfba-154">Create the user account before installing the file, registry key, folder or service being secured.</span></span>

<span data-ttu-id="7bfba-155">Если LockObject и пара таблиц в этой таблице имеют более одного условного выражения, результатом которого является значение true, установка завершается сбоем и установщик Windows возвращает сообщение об ошибке 1942.</span><span class="sxs-lookup"><span data-stu-id="7bfba-155">If a LockObject and Table pair in this table has more than one conditional expression that evaluates to true, the installation fails and Windows Installer returns an error message 1942.</span></span>

<span data-ttu-id="7bfba-156">Если строка [форматтедсддлтекст](formattedsddltext.md) в поле сддлтекст не может быть разрешена в допустимую строку SDDL, установка завершается сбоем и установщик Windows возвращает сообщение об ошибке 1943.</span><span class="sxs-lookup"><span data-stu-id="7bfba-156">If the [FormattedSDDLText](formattedsddltext.md) string in the SDDLText field cannot be resolved into a valid SDDL string, the installation fails and Windows Installer returns an error message 1943.</span></span>

<span data-ttu-id="7bfba-157">Если у пользователя недостаточно прав для задания дескриптора безопасности, указанного в поле Сддлтекст файла или папки, установка завершается ошибкой, а установщик Windows возвращает сообщение об ошибке 1926.</span><span class="sxs-lookup"><span data-stu-id="7bfba-157">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a file or folder, the installation fails and Windows Installer returns an error message 1926.</span></span>

<span data-ttu-id="7bfba-158">Если у пользователя недостаточно прав для задания дескриптора безопасности, указанного в поле Сддлтекст раздела реестра, установка завершается ошибкой, а установщик Windows возвращает сообщение об ошибке 1401.</span><span class="sxs-lookup"><span data-stu-id="7bfba-158">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a registry key, the installation fails and Windows Installer returns an error message 1401.</span></span>

<span data-ttu-id="7bfba-159">Если у пользователя недостаточно прав для задания дескриптора безопасности, указанного в поле Сддлтекст службы, установка завершается ошибкой, а установщик Windows возвращает сообщение об ошибке 1944.</span><span class="sxs-lookup"><span data-stu-id="7bfba-159">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a service, the installation fails and Windows Installer returns an error message 1944.</span></span>

## <a name="validation"></a><span data-ttu-id="7bfba-160">Проверка</span><span class="sxs-lookup"><span data-stu-id="7bfba-160">Validation</span></span>

<dl>

[<span data-ttu-id="7bfba-161">ICE104</span><span class="sxs-lookup"><span data-stu-id="7bfba-161">ICE104</span></span>](ice-104.md)  
[<span data-ttu-id="7bfba-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="7bfba-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7bfba-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="7bfba-163">ICE06</span></span>](ice06.md)  
</dl>

 

 
