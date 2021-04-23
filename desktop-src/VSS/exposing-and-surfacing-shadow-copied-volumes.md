---
description: Помимо доступа через интерфейс Ивссбаккупкомпонентс с помощью объекта устройства копии, инициатор запроса может сделать теневую копию доступной для других процессов в качестве подключенного устройства только для чтения.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Предоставление и отображая теневых скопированных томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693646"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a><span data-ttu-id="87e4d-103">Предоставление и отображая теневых скопированных томов</span><span class="sxs-lookup"><span data-stu-id="87e4d-103">Exposing and Surfacing Shadow Copied Volumes</span></span>

<span data-ttu-id="87e4d-104">Помимо доступа через интерфейс [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) с помощью [*объекта устройства*](vssgloss-d.md)копии, инициатор запроса может сделать теневую копию доступной для других процессов в качестве подключенного устройства только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87e4d-104">In addition to being accessed through the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface by means of its copy's [*device object*](vssgloss-d.md), a requester can make a shadow copy available to other processes as a mounted read-only device.</span></span>

<span data-ttu-id="87e4d-105">Этот процесс называется [*предоставлением теневой копии*](vssgloss-e.md)и выполняется с помощью метода [**Ивссбаккупкомпонентс:: експосеснапшот**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .</span><span class="sxs-lookup"><span data-stu-id="87e4d-105">This process is known as [*exposing a shadow copy*](vssgloss-e.md), and is performed using the [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) method.</span></span>

<span data-ttu-id="87e4d-106">Теневая копия может быть предоставлена как локальный том, назначенная буква диска или связанная с подключенной папкой, или как общая папка.</span><span class="sxs-lookup"><span data-stu-id="87e4d-106">A shadow copy can be exposed as a local volume—assigned a drive letter or associated with a mounted folder—or as a file share.</span></span>

<span data-ttu-id="87e4d-107">Чтобы проиллюстрировать это, рассмотрите возможность создания теневой копии тома в системе Експоседсис, подключенного к F:, \\ корневым каталогом которого являются каталоги дироне и диртво, а также файл филеоне.</span><span class="sxs-lookup"><span data-stu-id="87e4d-107">To illustrate, consider a shadow copy made of a volume on the system exposedSys mounted at F:\\ on whose root are the directories dirOne and dirTwo, and the file FileOne.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="87e4d-108">Локальное предоставление теневой копии</span><span class="sxs-lookup"><span data-stu-id="87e4d-108">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="87e4d-109">При подключении в качестве локального тома корень теневой копии всегда отображается в точке подключения (буква диска или подключенная папка), и все теневые копии файлов видимы.</span><span class="sxs-lookup"><span data-stu-id="87e4d-109">When mounted as a local volume, the shadow copy's root is always visible at the mount point (drive letter or mounted folder) and all the shadow-copied files are visible.</span></span>

<span data-ttu-id="87e4d-110">Если теневая копия была локально предоставлена через подключенную папку C: \\ шадовофф, можно найти все файлы на диске, подключенные к диску F: \\ на момент создания теневой копии, доступной в разделе C: \\ шадовофф.</span><span class="sxs-lookup"><span data-stu-id="87e4d-110">If the shadow copy was locally exposed through the mounted folder C:\\ShadowOfF, you would find all files present on disk mounted at F:\\ at the time of the shadow copy available under C:\\ShadowOfF.</span></span> <span data-ttu-id="87e4d-111">При проверке C: \\ шадовофф будут раскрыты два каталога, дироне и диртво и один файл филеоне в C: \\ шадовофф.</span><span class="sxs-lookup"><span data-stu-id="87e4d-111">Examining C:\\ShadowOfF would reveal two directories, dirOne and dirTwo, and one file, fileOne, under C:\\ShadowOfF.</span></span>

<span data-ttu-id="87e4d-112">Для локального предоставления теневого копирования можно использовать следующие вызовы:</span><span class="sxs-lookup"><span data-stu-id="87e4d-112">A call to locally expose the shadow copy might be:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="87e4d-113">Если теневая копия была успешно открыта локально, *всзекспосед* должна содержать строку расширенных символов "C: \\ шадовофф".</span><span class="sxs-lookup"><span data-stu-id="87e4d-113">If the shadow copy was successfully exposed locally, *wszExposed* should contain the wide character string "C:\\ShadowOfF."</span></span>

<span data-ttu-id="87e4d-114">После этого теневая копия может быть недоступна путем вызова [**IVssBackupComponentsEx2:: унекспосеснапшот**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="87e4d-114">The shadow copy can later be unexposed by calling [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span></span>

<span data-ttu-id="87e4d-115">Локально можно предоставить доступ только к постоянным теневым копиям, то есть теневым копиям, созданным с помощью отката \_ CTX \_ NAS \_ или \_ \_ отката приложения CTX в VSS \_ .</span><span class="sxs-lookup"><span data-stu-id="87e4d-115">Only persistent shadow copies—that is, shadow copies created with either VSS\_CTX\_NAS\_ROLLBACK or VSS\_CTX\_APP\_ROLLBACK—can be exposed locally.</span></span>

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a><span data-ttu-id="87e4d-116">Предоставление теневой копии в качестве удаленной общей папки</span><span class="sxs-lookup"><span data-stu-id="87e4d-116">Exposing a Shadow Copy as a Remote Share</span></span>

<span data-ttu-id="87e4d-117">Кроме того, можно выбрать создание теневой копии диска, подключенного к \\ , в качестве удаленной общей папки, и предоставить только данные в разделе диртво в качестве общей папки диртвуфф.</span><span class="sxs-lookup"><span data-stu-id="87e4d-117">Alternatively, you could choose to make the shadow copy of the disk mounted at F:\\ available as a remote file share, and expose only data under dirTwo as the file share dirTwoOfF.</span></span>

<span data-ttu-id="87e4d-118">В этом случае система может получить доступ к теневой копии файлов в папке F: \\ диртво, сопоставляя \\ \\ експоседсис \\ диртвуфф как сетевой диск.</span><span class="sxs-lookup"><span data-stu-id="87e4d-118">In this case, systems could access the shadow copy of files under F:\\dirTwo by mapping \\\\exposedSys\\dirTwoOfF as a network drive.</span></span>

<span data-ttu-id="87e4d-119">Вызов для реализации удаленного доступа к теневой копии в качестве общей папки может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="87e4d-119">A call to implement remote exposing the shadow copy as a share might be the following:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="87e4d-120">Если теневая копия была успешно предоставлена удаленно, *всзекспосед* должна содержать строку расширенных символов "диртвуфф".</span><span class="sxs-lookup"><span data-stu-id="87e4d-120">If the shadow copy was successfully exposed remotely, *wszExposed* should contain the wide character string "dirTwoOfF."</span></span>

<span data-ttu-id="87e4d-121">Любая система, в настоящее время сопоставленная с сетевой папкой Диртвуфф, может отключиться от нее, так как она может отключиться от любой обычной общей папки.</span><span class="sxs-lookup"><span data-stu-id="87e4d-121">Any system currently mapping the network share of dirTwoOfF could disconnect from it, just as it might disconnect from any ordinary share.</span></span>

## <a name="surfacing-a-shadow-copy"></a><span data-ttu-id="87e4d-122">Отображая теневую копию</span><span class="sxs-lookup"><span data-stu-id="87e4d-122">Surfacing a Shadow Copy</span></span>

<span data-ttu-id="87e4d-123">[*Область теневой копии*](vssgloss-s.md) , в которой находится теневая копия, известна пространству имен диспетчера подключений системы.</span><span class="sxs-lookup"><span data-stu-id="87e4d-123">A [*surfaced shadow copy*](vssgloss-s.md) is one in which the shadow copy is known to a system's Mount Manager namespace.</span></span>

<span data-ttu-id="87e4d-124">Это означает, что такие теневые копии можно найти так же, как и любой другой доступный, но еще не подключенный том — с помощью **финдфирстволуме** и **финднекстволуме**, например.</span><span class="sxs-lookup"><span data-stu-id="87e4d-124">This means that you can locate such shadow copies just as you would locate any other available but not-yet-mounted volume—by using **FindFirstVolume** and **FindNextVolume**, for example.</span></span>

<span data-ttu-id="87e4d-125">Очевидно, что теневые копии также отображаются на теневых копиях.</span><span class="sxs-lookup"><span data-stu-id="87e4d-125">Clearly, then, exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="87e4d-126">Однако обратный порядок не обязательно должен быть истинным.</span><span class="sxs-lookup"><span data-stu-id="87e4d-126">However, the reverse is not necessarily true.</span></span>

<span data-ttu-id="87e4d-127">Если удаленная локально доступная теневая копия была отключена или система решила отсоединить удаленно открытую теневую копию, эта теневая копия больше не будет предоставляться.</span><span class="sxs-lookup"><span data-stu-id="87e4d-127">If a locally exposed shadow copy was dismounted, or a system chose to disconnect a remotely exposed shadow copy, that shadow copy would no longer be exposed.</span></span> <span data-ttu-id="87e4d-128">Тем не менее, если теневая копия сохранена, отображаются тома.</span><span class="sxs-lookup"><span data-stu-id="87e4d-128">However, as long as the shadow copy persisted, the volumes would be surfaced.</span></span> <span data-ttu-id="87e4d-129">Это означает, что они могут быть подключены так же, как и любые другие тома только для чтения.</span><span class="sxs-lookup"><span data-stu-id="87e4d-129">This means they could be mounted like any other read-only volume.</span></span>

 

 



