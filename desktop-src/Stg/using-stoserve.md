---
title: Использование Стосерве
description: Стосерве — это библиотека DLL, которая в основном предназначена для COM-сервера.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661769"
---
# <a name="using-stoserve"></a><span data-ttu-id="bea6f-103">Использование Стосерве</span><span class="sxs-lookup"><span data-stu-id="bea6f-103">Using StoServe</span></span>

<span data-ttu-id="bea6f-104">**Стосерве** — это библиотека DLL, которая в основном предназначена для COM-сервера.</span><span class="sxs-lookup"><span data-stu-id="bea6f-104">**StoServe** is a DLL that is intended primarily as a COM server.</span></span> <span data-ttu-id="bea6f-105">Хотя он может быть неявно загружен путем связывания со связанным с ним. LIB-файл обычно используется после явного вызова LoadLibrary, обычно из COM-функции [**кожетклассобжект**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span><span class="sxs-lookup"><span data-stu-id="bea6f-105">Although it can be implicitly loaded by linking to its associated .LIB file, it is normally used after an explicit LoadLibrary call, usually from within the COM function [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span></span> <span data-ttu-id="bea6f-106">**Стосерве** — это самостоятельная регистрация внутрипроцессного сервера.</span><span class="sxs-lookup"><span data-stu-id="bea6f-106">**StoServe** is a self-registering in-process server.</span></span>

<span data-ttu-id="bea6f-107">Чтобы использовать **стосерве**, клиентской программе не нужно включать стосерве. H или ссылку на СТОСЕРВЕ. LIB.</span><span class="sxs-lookup"><span data-stu-id="bea6f-107">To use **StoServe**, a client program does not need to include STOSERVE.H or link to STOSERVE.LIB.</span></span> <span data-ttu-id="bea6f-108">COM-клиент **стосерве** получает доступ исключительно через CLSID объекта и службы COM.</span><span class="sxs-lookup"><span data-stu-id="bea6f-108">A COM client of **StoServe** obtains access solely through its object's CLSID and COM services.</span></span> <span data-ttu-id="bea6f-109">Для **стосерве** этот CLSID является CLSID \_ дллпапер (ОПРЕДЕЛЕН в файле папгуидс. H в \\ каталоге с общим родителем Inc.)</span><span class="sxs-lookup"><span data-stu-id="bea6f-109">For **StoServe**, that CLSID is CLSID\_DllPaper (defined in file PAPGUIDS.H in the \\INC sibling directory).</span></span> <span data-ttu-id="bea6f-110">В примере кода [стоклиен](structured-storage-client-sample--stoclien-.md) показано, как клиент получает этот доступ.</span><span class="sxs-lookup"><span data-stu-id="bea6f-110">The [StoClien](structured-storage-client-sample--stoclien-.md) code sample shows how the client obtains this access.</span></span>

<span data-ttu-id="bea6f-111">Файл makefile, который создает этот пример, автоматически регистрирует сервер в реестре.</span><span class="sxs-lookup"><span data-stu-id="bea6f-111">The makefile that builds this sample automatically registers the server in the registry.</span></span> <span data-ttu-id="bea6f-112">Можно вручную инициировать самостоятельную регистрацию, выполнив следующую команду в командной строке в каталоге **стосерве** :</span><span class="sxs-lookup"><span data-stu-id="bea6f-112">You can manually initiate its self-registration by issuing the following command at the command prompt in the **StoServe** directory:</span></span>

<span data-ttu-id="bea6f-113"> **Регистрация** NMAKE</span><span class="sxs-lookup"><span data-stu-id="bea6f-113">**nmake** **register**</span></span>

<span data-ttu-id="bea6f-114">При этом предполагается, что среда компиляции настроена.</span><span class="sxs-lookup"><span data-stu-id="bea6f-114">This assumes that you have a compilation environment set up.</span></span> <span data-ttu-id="bea6f-115">Если нет, можно также напрямую вызвать команду REGISTER.EXE в командной строке, находясь в каталоге **стосерве** .</span><span class="sxs-lookup"><span data-stu-id="bea6f-115">If not, you can also directly invoke the REGISTER.EXE command at the command prompt while in the **StoServe** directory.</span></span>

<span data-ttu-id="bea6f-116">**..\\ регистрация \\register.exe** **stoserve.dll**</span><span class="sxs-lookup"><span data-stu-id="bea6f-116">**..\\register\\register.exe** **stoserve.dll**</span></span>

<span data-ttu-id="bea6f-117">Для этих команд регистрации требуется предварительная сборка образца REGISTER в этой серии, а также предыдущие сборки STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="bea6f-117">These registration commands require a prior build of the REGISTER sample in this series, as well as a prior build of STOSERVE.DLL.</span></span>

<span data-ttu-id="bea6f-118">В этой серии файлы Makefile используют служебную программу REGISTER.EXE из примера REGISTER.</span><span class="sxs-lookup"><span data-stu-id="bea6f-118">In this series, the makefiles use the REGISTER.EXE utility from the REGISTER sample.</span></span> <span data-ttu-id="bea6f-119">Последние выпуски пакета SDK платформы и Visual C++ включают служебную программу REGSVR32.EXE, которая может использоваться аналогичным образом для регистрации серверов обработки и упаковки библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="bea6f-119">Recent releases of the Platform Software Development Kit (SDK) and Visual C++ include a utility, REGSVR32.EXE, which can be used in a similar fashion to register in-process servers and marshaling DLLs.</span></span>

<span data-ttu-id="bea6f-120">**Стосерве** использует многие служебные классы и службы, предоставляемые аппутил.</span><span class="sxs-lookup"><span data-stu-id="bea6f-120">**StoServe** uses many of the utility classes and services provided by APPUTIL.</span></span> <span data-ttu-id="bea6f-121">Чтобы получить дополнительные сведения о АППУТИЛ, изучите исходный код библиотеки АППУТИЛ в каталоге одноуровневых АППУТИЛ и APPUTIL.HTM в главном каталоге Tutorial.</span><span class="sxs-lookup"><span data-stu-id="bea6f-121">For more details on APPUTIL, study the APPUTIL library's source code in the sibling APPUTIL directory and APPUTIL.HTM in the main tutorial directory.</span></span>

 

 