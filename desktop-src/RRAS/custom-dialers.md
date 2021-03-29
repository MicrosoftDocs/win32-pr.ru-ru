---
title: Пользовательские номеронабирателя
description: Windows 2000 и более поздние операционные системы позволяют разработчикам предоставлять собственные настраиваемые номеронабирателя, работающие со службой удаленного доступа (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Пользовательские номеронабирателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260958"
---
# <a name="custom-dialers"></a><span data-ttu-id="c26f7-104">Пользовательские номеронабирателя</span><span class="sxs-lookup"><span data-stu-id="c26f7-104">Custom Dialers</span></span>

<span data-ttu-id="c26f7-105">Windows 2000 и более поздние операционные системы позволяют разработчикам предоставлять собственные настраиваемые номеронабирателя, работающие со службой удаленного доступа (RAS).</span><span class="sxs-lookup"><span data-stu-id="c26f7-105">Windows 2000 and later operating systems enable developers to provide their own custom dialers that work with the Remote Access Service (RAS).</span></span> <span data-ttu-id="c26f7-106">Пользовательский номеронабиратель реализуется в виде одной библиотеки динамической компоновки (DLL), которая экспортирует следующие точки входа:</span><span class="sxs-lookup"><span data-stu-id="c26f7-106">The custom dialer is implemented as a single dynamic-link library (DLL) that exports the following entry points:</span></span>

-   [<span data-ttu-id="c26f7-107">**раскустомдиал**</span><span class="sxs-lookup"><span data-stu-id="c26f7-107">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [<span data-ttu-id="c26f7-108">**раскустомдиалдлг**</span><span class="sxs-lookup"><span data-stu-id="c26f7-108">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [<span data-ttu-id="c26f7-109">**раскустомхангуп**</span><span class="sxs-lookup"><span data-stu-id="c26f7-109">**RasCustomHangup**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [<span data-ttu-id="c26f7-110">**раскустоментридлг**</span><span class="sxs-lookup"><span data-stu-id="c26f7-110">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [<span data-ttu-id="c26f7-111">**раскустомделетинтринотифи**</span><span class="sxs-lookup"><span data-stu-id="c26f7-111">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

<span data-ttu-id="c26f7-112">Библиотека DLL пользовательского вызова должна экспортировать все эти точки входа и должна реализовывать точки входа как функции Юникода.</span><span class="sxs-lookup"><span data-stu-id="c26f7-112">The custom-dial DLL must export all of these entry points, and it must implement the entry points as Unicode functions.</span></span> <span data-ttu-id="c26f7-113">Дополнительные сведения об этих функциях см. на странице справки по каждой функции в Windows SDK ссылки на службу удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="c26f7-113">For more information about these functions, see the reference page for each function in the Windows SDK Remote Access Service Reference.</span></span>

<span data-ttu-id="c26f7-114">Чтобы подключение службы удаленного доступа использует пользовательский номеронабиратель, запись телефонной книги для подключения должна содержать путь к DLL-библиотеке пользовательского набора.</span><span class="sxs-lookup"><span data-stu-id="c26f7-114">In order for a RAS connection to use the custom dialer, the phone-book entry for the connection must contain the path to the custom-dial DLL.</span></span> <span data-ttu-id="c26f7-115">Используйте функции API RAS [**расжетентрипропертиес**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) и [**рассетентрипропертиес**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) , чтобы задать этот путь в элементе **сзкустомдиалдлл** структуры [**расентри**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) для записи телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="c26f7-115">Use the RAS API functions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) to set this path in the **szCustomDialDll** member of the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure for the phone-book entry.</span></span>

## <a name="updating-the-registry-for-custom-dialers"></a><span data-ttu-id="c26f7-116">Обновление реестра для пользовательских номеронабирателя</span><span class="sxs-lookup"><span data-stu-id="c26f7-116">Updating the Registry for Custom Dialers</span></span>

<span data-ttu-id="c26f7-117">Чтобы система набирает соединение, использующее пользовательский номеронабиратель, путь к DLL-библиотеке пользовательского вызова должен существовать в следующем параметре реестра.</span><span class="sxs-lookup"><span data-stu-id="c26f7-117">In order for the system to dial a connection that uses a custom dialer, the path to the custom-dial DLL must exist in the following registry value.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

<span data-ttu-id="c26f7-118">Так как **кустомдлл** имеет тип **reg \_ Multi \_ SZ**, он может хранить пути к нескольким библиотекам DLL с пользовательским набором.</span><span class="sxs-lookup"><span data-stu-id="c26f7-118">Because **CustomDLL** is of type **REG\_MULTI\_SZ**, it can hold paths to multiple custom-dial DLLs.</span></span> <span data-ttu-id="c26f7-119">В дополнение к записи телефонной книги для подключения необходимо задать путь к библиотеке DLL пользовательского вызова в этом параметре реестра.</span><span class="sxs-lookup"><span data-stu-id="c26f7-119">You need to set the path to the custom-dial DLL in this registry value, in addition to the phone-book entry for the connection.</span></span>

<span data-ttu-id="c26f7-120">По умолчанию это значение реестра доступно для записи только пользователю с правами администратора или системными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="c26f7-120">By default, this registry value is writeable only by a user with Administrator or System privileges.</span></span> <span data-ttu-id="c26f7-121">В целях безопасности не изменяйте разрешения для этого раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="c26f7-121">For security reasons, do not change the permissions on this registry key.</span></span>

## <a name="using-custom-dialers-at-system-logon"></a><span data-ttu-id="c26f7-122">Использование пользовательских номеронабирателя при входе в систему</span><span class="sxs-lookup"><span data-stu-id="c26f7-122">Using Custom Dialers at System Logon</span></span>

<span data-ttu-id="c26f7-123">Windows 2000 и более поздние операционные системы позволяют пользователю устанавливать подключение RAS во время входа в систему.</span><span class="sxs-lookup"><span data-stu-id="c26f7-123">Windows 2000 and later operating systems allow a user to establish a RAS connection at the time of logon.</span></span> <span data-ttu-id="c26f7-124">Для этого пользователь проверяет **Вход с помощью удаленного доступа к сети** в диалоговом окне " **сведения о входе** ".</span><span class="sxs-lookup"><span data-stu-id="c26f7-124">To do so, the user checks **Logon using Dial-up Networking** in the **Logon Information** dialog box.</span></span> <span data-ttu-id="c26f7-125">Когда пользователь нажмет кнопку "ОК", система отобразит доступные подключения.</span><span class="sxs-lookup"><span data-stu-id="c26f7-125">After the user clicks the Okay button, the system displays the available connections.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="c26f7-126">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="c26f7-126">Security Considerations</span></span>

<span data-ttu-id="c26f7-127">В большинстве случаев пользовательский номеронабиратель работает с привилегиями безопасности пользователя, который его вызывает.</span><span class="sxs-lookup"><span data-stu-id="c26f7-127">In most cases, a custom dialer operates with the security privileges of the user that invokes it.</span></span> <span data-ttu-id="c26f7-128">Однако если пользовательский номеронабиратель вызывается при входе в систему, он работает с системными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="c26f7-128">However, if the custom dialer is invoked at logon, it operates with system privileges.</span></span> <span data-ttu-id="c26f7-129">Поэтому создайте пользовательский номеронабиратель, чтобы он не был использован для нарушения безопасности системы.</span><span class="sxs-lookup"><span data-stu-id="c26f7-129">Therefore, design the custom dialer so that it cannot be used to violate system security.</span></span> <span data-ttu-id="c26f7-130">Например, набор не должен представлять пользовательский интерфейс, позволяющий пользователю записывать доступ к файловой системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="c26f7-130">For example, the dialer should not present a user interface that allows the user write access to the computer's file system.</span></span> <span data-ttu-id="c26f7-131">Пользовательские интерфейсы, предоставляющие такой доступ, включают в себя диалоговое окно **find-file** , общее диалоговое окно **открытия файла** и **справку** Windows.</span><span class="sxs-lookup"><span data-stu-id="c26f7-131">User interfaces that provide such access include the **Find-File** dialog, the **File-Open** common dialog, and Windows **Help**.</span></span>

## <a name="custom-dialer-user-interface-must-support-idcancel"></a><span data-ttu-id="c26f7-132">Пользовательский интерфейс пользовательского номеронабирателя должен поддерживать ИДКАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="c26f7-132">Custom Dialer User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="c26f7-133">Если пользовательский номеронабиратель отображает пользовательский интерфейс, Пользовательский интерфейс должен поддерживать \_ Командные сообщения WM, где ловорд (*wParam*) равняется идканцел.</span><span class="sxs-lookup"><span data-stu-id="c26f7-133">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

 

 