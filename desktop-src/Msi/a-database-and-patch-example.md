---
description: Приложение может использовать функцию Мсиопендатабасе для открытия новой или существующей базы данных установки (MSI-файла) или пакета исправлений (MSP-файл). Приложение проверяет возвращаемое значение Мсиопендатабасе перед использованием маркера базы данных.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Пример базы данных и исправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662981"
---
# <a name="a-database-and-patch-example"></a><span data-ttu-id="0a3f2-103">Пример базы данных и исправления</span><span class="sxs-lookup"><span data-stu-id="0a3f2-103">A Database and Patch Example</span></span>

<span data-ttu-id="0a3f2-104">Приложение может использовать функцию [**мсиопендатабасе**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) для открытия новой или существующей базы данных установки (MSI-файла) или пакета исправлений (MSP-файл). Приложение проверяет возвращаемое значение **мсиопендатабасе** перед использованием маркера базы данных.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-104">An application can use the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function to open a new or existing installation database (.msi file) or patch package (.msp file.) The application checks the return value of **MsiOpenDatabase** before using the database handle.</span></span>

<span data-ttu-id="0a3f2-105">В следующих примерах используются переменные типа **пмсихандле** , определенные в MSI. h.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-105">The following examples use the **PMSIHANDLE** type variables defined in msi.h.</span></span> <span data-ttu-id="0a3f2-106">Рекомендуется использовать тип **пмсихандле** , так как установщик закрывает объекты **пмсихандле** , когда они выходят за пределы области действия, тогда как приложение должно закрыть объекты **мсихандле** , вызвав [**мсиклосехандле**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span><span class="sxs-lookup"><span data-stu-id="0a3f2-106">It is recommended to use the **PMSIHANDLE** type because the installer closes **PMSIHANDLE** objects as they go out of scope, whereas your application must close **MSIHANDLE** objects by calling [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span></span> <span data-ttu-id="0a3f2-107">Дополнительные сведения см. в разделе [Использование пмсихандле вместо Handle](windows-installer-best-practices.md) в [рекомендациях по установщик Windows](windows-installer-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="0a3f2-107">For more information see [Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) section in the [Windows Installer Best Practices](windows-installer-best-practices.md).</span></span>

<span data-ttu-id="0a3f2-108">В следующем примере открывается база данных, sample.msi, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-108">The following example opens a database, sample.msi, for reading only.</span></span> <span data-ttu-id="0a3f2-109">[**Мсиопендатабасе**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) выполняется, только если sample.msi существует в каталоге c: \\ Test.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) succeeds only if sample.msi exists in the c:\\test directory.</span></span> <span data-ttu-id="0a3f2-110">После успешного выполнения возвращенный обработчик базы данных можно использовать для запроса данных в пакете установки с помощью [**мсидатабасеопенвиев**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) и [**мсижетсуммаринформатион**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span><span class="sxs-lookup"><span data-stu-id="0a3f2-110">Upon success, the returned database handle can be used to query the data in the installation package using [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) and [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span></span>


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



<span data-ttu-id="0a3f2-111">В следующем примере открывается база данных для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-111">The following example opens the database for reading and writing.</span></span> <span data-ttu-id="0a3f2-112">Если приложение вызывает [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), сохраняются все изменения, внесенные в базу данных.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-112">If the application calls [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), all changes made to the database are saved.</span></span> <span data-ttu-id="0a3f2-113">Если приложение не вызывает **мсидатабасекоммит**, в базу данных не вносятся изменения.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-113">If the application does not call **MsiDatabaseCommit**, no changes are made to the database.</span></span>


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



<span data-ttu-id="0a3f2-114">В следующем примере берется существующая база данных, text.msi и создается новая база данных newtest.msi.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-114">The following example takes an existing database, text.msi, and creates a new database, newtest.msi.</span></span> <span data-ttu-id="0a3f2-115">Любые внесенные изменения можно сохранить в новой базе данных, вызвав [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="0a3f2-115">Any changes that are made can be saved in the new database by calling [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="0a3f2-116">Существующая база данных, указанная в параметре *сздатабасепас* , не изменена.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-116">The existing database specified in the *szDatabasePath* parameter is unchanged.</span></span>


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



<span data-ttu-id="0a3f2-117">В следующем примере открывается пакет исправлений установщик Windows (MSP-файл) только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-117">The following example opens a Windows Installer patch package (.msp file) for reading only.</span></span> <span data-ttu-id="0a3f2-118">Возвращенный маркер исправления можно использовать для определения ящиков и преобразования подхранилищ, включенных в пакет исправлений, с помощью запросов к таблицам [ \_ Streams](-streams-table.md) и [ \_ Storage](-storages-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0a3f2-118">The returned patch handle can be used to determine the cabinets and transform substorages included in the patch package by queries on the [\_Streams](-streams-table.md) and [\_Storages](-storages-table.md) tables.</span></span>

<span data-ttu-id="0a3f2-119">**Установщик Windows 2,0:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-119">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="0a3f2-120">Начиная с установщик Windows 3,0, приложение может запрашивать [таблицу мсипатчсекуенце](msipatchsequence-table.md) , присутствующую в пакете исправлений, который использует новые сведения о последовательности исправлений.</span><span class="sxs-lookup"><span data-stu-id="0a3f2-120">Beginning with Windows Installer 3.0, the application can query the [MsiPatchSequence table](msipatchsequence-table.md) present in a patch package that uses the new patch sequencing information.</span></span>


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



