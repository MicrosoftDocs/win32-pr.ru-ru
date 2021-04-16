---
description: Настраиваемые действия могут добавлять сведения о времени и ходе выполнения в элемент управления ProgressBar. Дополнительные сведения о создании диалогового окна "Отображение действий" с ProgressBar см. в разделе Разработка элемента управления ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Добавление настраиваемых действий в ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650740"
---
# <a name="adding-custom-actions-to-the-progressbar"></a><span data-ttu-id="5387c-104">Добавление настраиваемых действий в ProgressBar</span><span class="sxs-lookup"><span data-stu-id="5387c-104">Adding Custom Actions to the ProgressBar</span></span>

<span data-ttu-id="5387c-105">[Настраиваемые действия](custom-actions.md) могут добавлять сведения о времени и ходе выполнения в элемент управления [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="5387c-105">[Custom Actions](custom-actions.md) can add time and progress information to a [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="5387c-106">Дополнительные сведения о создании диалогового окна "Отображение действий" с ProgressBar см. в разделе [Разработка элемента управления ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="5387c-106">For more information about creating an action display dialog box having a ProgressBar, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

<span data-ttu-id="5387c-107">Обратите внимание, что в пакет установщик Windows необходимо добавить два настраиваемых действия, чтобы точно сообщить о времени и ходе выполнения элементу ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="5387c-107">Note that two custom actions must be added to the Windows Installer package to accurately report time and progress information to the ProgressBar.</span></span> <span data-ttu-id="5387c-108">Одно настраиваемое действие должно быть отложенным пользовательским действием.</span><span class="sxs-lookup"><span data-stu-id="5387c-108">One custom action must be a deferred custom action.</span></span> <span data-ttu-id="5387c-109">Это пользовательское действие должно завершить пользовательскую установку и отправить в элемент управления [ProgressBar](progressbar-control.md) объем отдельных приращений, когда установщик запустит сценарий установки.</span><span class="sxs-lookup"><span data-stu-id="5387c-109">This custom action should complete your custom installation and send the amounts of individual increments to the [ProgressBar](progressbar-control.md) control when the installer runs the installation script.</span></span> <span data-ttu-id="5387c-110">Второе настраиваемое действие должно быть немедленным настраиваемым действием, которое информирует ProgressBar о том, сколько тактов следует добавить к общему числу на этапе создания сценария для установки.</span><span class="sxs-lookup"><span data-stu-id="5387c-110">The second custom action must be an immediate execution custom action that informs the ProgressBar how many ticks to add to the total count during the acquisition and script generation phase of the installation.</span></span>

<span data-ttu-id="5387c-111">**Добавление настраиваемого действия в ProgressBar**</span><span class="sxs-lookup"><span data-stu-id="5387c-111">**To add a custom action to the ProgressBar**</span></span>

1.  <span data-ttu-id="5387c-112">Определите, как настраиваемое действие будет описывать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="5387c-112">Decide how the custom action will describe its progress.</span></span> <span data-ttu-id="5387c-113">Например, пользовательское действие, устанавливающее разделы реестра, может отображать сообщение о ходе выполнения и обновлять компонент [ProgressBar](progressbar-control.md) каждый раз, когда установщик записывает один раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="5387c-113">For example, a custom action that installs registry keys could display a progress message and update the [ProgressBar](progressbar-control.md) each time the installer writes one registry key.</span></span>
2.  <span data-ttu-id="5387c-114">Каждое обновление с помощью настраиваемого действия изменяет длину элемента [ProgressBar](progressbar-control.md) на постоянное приращение.</span><span class="sxs-lookup"><span data-stu-id="5387c-114">Each update by the custom action changes the length of the [ProgressBar](progressbar-control.md) by a constant increment.</span></span> <span data-ttu-id="5387c-115">Укажите или Вычислите количество тактов в каждом приращении.</span><span class="sxs-lookup"><span data-stu-id="5387c-115">Specify or calculate the number of ticks in each increment.</span></span> <span data-ttu-id="5387c-116">Как правило, изменение в элементе ProgressBar длины одного тика соответствует установке одного байта.</span><span class="sxs-lookup"><span data-stu-id="5387c-116">Typically a change in ProgressBar length of one tick corresponds to the installation of one byte.</span></span> <span data-ttu-id="5387c-117">Например, если установщик устанавливает примерно 10000 байт при записи одного раздела реестра, можно указать, что увеличивается такт 10000.</span><span class="sxs-lookup"><span data-stu-id="5387c-117">For example, if the installer installs approximately 10000 bytes when it writes one registry key, you can specify that there are 10000 ticks in an increment.</span></span>
3.  <span data-ttu-id="5387c-118">Укажите или Вычислите общее число тактов, добавляемое настраиваемым действием в длину [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="5387c-118">Specify or calculate the total number of ticks the custom action adds to the length of the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="5387c-119">Число тактов, добавленных настраиваемым действием, обычно вычисляется следующим образом: (шаг деления) x (число элементов).</span><span class="sxs-lookup"><span data-stu-id="5387c-119">The number of ticks added by the custom action is usually calculated as: (tick increment) x (number of items).</span></span> <span data-ttu-id="5387c-120">Например, если пользовательское действие записывает 10 разделов реестра, установщик установит примерно 100000 байт, поэтому установщик должен увеличить оценку итоговой общей длины ProgressBar на 100000 тактов.</span><span class="sxs-lookup"><span data-stu-id="5387c-120">For example, if the custom action writes 10 registry keys, the installer installs approximately 100000 bytes and the installer therefore must increase the estimate of the final total length of the ProgressBar by 100000 ticks.</span></span>
    > [!Note]  
    > <span data-ttu-id="5387c-121">Для динамического вычисления пользовательское действие должно содержать раздел, который сразу же выполняется во время создания скрипта.</span><span class="sxs-lookup"><span data-stu-id="5387c-121">To calculate this dynamically, the custom action must contain a section that is immediately executed during script generation.</span></span> <span data-ttu-id="5387c-122">Количество тактов, сообщаемое настраиваемым действием отложенного выполнения, должно быть равно числу тактов, добавляемых к общему количеству тактов в результате немедленного выполнения.</span><span class="sxs-lookup"><span data-stu-id="5387c-122">The amount of ticks reported by your deferred execution custom action must be equal to the number of ticks added to the total tick count by the immediate execution action.</span></span> <span data-ttu-id="5387c-123">Если это не так, оставшееся время, которое сообщает элементу управления "текст TimeRemaining", будет неточным.</span><span class="sxs-lookup"><span data-stu-id="5387c-123">If this is not the case, the time remaining as reported by the TimeRemaining text control will be inaccurate.</span></span>

     

4.  <span data-ttu-id="5387c-124">Разделите настраиваемое действие на два раздела кода: раздел, который выполняется на этапе создания скрипта, и раздел, который выполняется на этапе выполнения установки.</span><span class="sxs-lookup"><span data-stu-id="5387c-124">Separate your custom action into two sections of code: a section that runs during the script generation phase and a section that runs during the execution phase of the installation.</span></span> <span data-ttu-id="5387c-125">Это можно сделать с помощью двух файлов или можно использовать один файл, выполнив условия в режиме выполнения установщика.</span><span class="sxs-lookup"><span data-stu-id="5387c-125">You can do this using two files or you can use one file by conditioning on the run mode of the installer.</span></span> <span data-ttu-id="5387c-126">В следующем примере используется один файл и проверяется состояние установки.</span><span class="sxs-lookup"><span data-stu-id="5387c-126">The following sample uses one file and checks the installation state.</span></span> <span data-ttu-id="5387c-127">Разделы примера зависят от того, находится ли установщик на этапе выполнения или создания сценария установки.</span><span class="sxs-lookup"><span data-stu-id="5387c-127">Sections of the sample are conditioned to run depending on whether the installer is in the execution or script generation phase of the installation.</span></span>
5.  <span data-ttu-id="5387c-128">Раздел, выполняемый во время создания скрипта, должен увеличить оценку итоговой общей длины элемента [ProgressBar](progressbar-control.md) на общее число тактов в настраиваемом действии.</span><span class="sxs-lookup"><span data-stu-id="5387c-128">The section that runs during script generation should increase the estimate of the final total length of the [ProgressBar](progressbar-control.md) by the total number of ticks in the custom action.</span></span> <span data-ttu-id="5387c-129">Это делается путем отправки сообщения о ходе выполнения **прогрессаддитион** .</span><span class="sxs-lookup"><span data-stu-id="5387c-129">This is done by sending a **ProgressAddition** progress message.</span></span>
6.  <span data-ttu-id="5387c-130">Раздел, выполняемый на этапе выполнения установки, должен настроить текст сообщения и шаблоны, чтобы информировать пользователя о действиях, выполняемых настраиваемым действием, и направить установщик на обновление элемента управления [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="5387c-130">The section that runs during the execution phase of installation should set up message text and templates to inform the user about what the custom action is doing and to direct the installer on updating the [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="5387c-131">Например, сообщите установщику о необходимости переместить компонент ProgressBar на один шаг вперед и отправить сообщение о ходе выполнения с каждым обновлением.</span><span class="sxs-lookup"><span data-stu-id="5387c-131">For example, inform the installer to move the ProgressBar forward one increment and send an explicit progress message with each update.</span></span> <span data-ttu-id="5387c-132">В этом разделе обычно есть цикл, если пользовательское действие устанавливает что-то.</span><span class="sxs-lookup"><span data-stu-id="5387c-132">There is usually a loop in this section if the custom action is installing something.</span></span> <span data-ttu-id="5387c-133">При каждом прохождении этого цикла установщик может установить один элемент ссылки, например раздел реестра, и обновить элемент управления ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="5387c-133">With each pass through this loop, the installer can install one reference item such as a registry key and update the ProgressBar control</span></span>
7.  <span data-ttu-id="5387c-134">Добавьте немедленный настраиваемое действие выполнения в пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="5387c-134">Add an immediate execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="5387c-135">Это пользовательское действие информирует компонент [ProgressBar](progressbar-control.md) о том, как он будет изменяться на этапах установки и создания сценариев.</span><span class="sxs-lookup"><span data-stu-id="5387c-135">This custom action informs the [ProgressBar](progressbar-control.md) how much to advance during the aquisition and script generation phases of the installation.</span></span> <span data-ttu-id="5387c-136">В следующем примере источником является библиотека DLL, созданная путем компиляции примера кода, а целевым объектом является точка входа Капрогресс.</span><span class="sxs-lookup"><span data-stu-id="5387c-136">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
8.  <span data-ttu-id="5387c-137">Добавьте настраиваемое действие отложенного выполнения в пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="5387c-137">Add a deferred execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="5387c-138">Это пользовательское действие выполняет шаги фактической установки и информирует [ProgressBar](progressbar-control.md) о том, сколько времени необходимо для того, чтобы на момент запуска скрипта установки выполнялся установщик.</span><span class="sxs-lookup"><span data-stu-id="5387c-138">This custom action completes the steps of the actual installation and informs the [ProgressBar](progressbar-control.md) how much to advance the bar at the time when the installer runs the installation script.</span></span> <span data-ttu-id="5387c-139">В следующем примере источником является библиотека DLL, созданная путем компиляции примера кода, а целевым объектом является точка входа Капрогресс.</span><span class="sxs-lookup"><span data-stu-id="5387c-139">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
9.  <span data-ttu-id="5387c-140">Запланируйте как настраиваемые действия между [инсталлинитиализе](installinitialize-action.md) и [функции InstallFinalize](installfinalize-action.md) в таблице [инсталлексекутесекуенце](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5387c-140">Schedule both custom actions between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the [InstallExecuteSequence](installexecutesequence-table.md) table.</span></span> <span data-ttu-id="5387c-141">Отложенное настраиваемое действие должно быть запланировано сразу после немедленного выполнения настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="5387c-141">The deferred custom action should be scheduled immediately after the immediate execution custom action.</span></span> <span data-ttu-id="5387c-142">Установщик не будет выполнять отложенное настраиваемое действие до выполнения скрипта.</span><span class="sxs-lookup"><span data-stu-id="5387c-142">The installer will not run the deferred custom action until the script is executed.</span></span>

<span data-ttu-id="5387c-143">В следующем примере показано, как можно добавить настраиваемое действие в [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="5387c-143">The following sample shows how a custom action can be added to the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="5387c-144">Источником настраиваемых действий является библиотека DLL, созданная путем компиляции образца кода, а целью обоих настраиваемых действий является точка входа Капрогресс.</span><span class="sxs-lookup"><span data-stu-id="5387c-144">The source of both custom actions is the DLL created by compiling the sample code and the target of both custom actions is the entry point, CAProgress.</span></span> <span data-ttu-id="5387c-145">Этот пример не вносит никаких изменений в систему, но работает с ProgressBar так, как если бы вы устанавливали 10 элементов ссылок, размер которых составляет примерно 10 000 байт.</span><span class="sxs-lookup"><span data-stu-id="5387c-145">This sample does not make any actual changes to the system, but operates the ProgressBar as if installing 10 reference items that are each approximately 10,000 bytes in size.</span></span> <span data-ttu-id="5387c-146">Установщик обновляет сообщение и компонент ProgressBar при каждом установке эталонного элемента.</span><span class="sxs-lookup"><span data-stu-id="5387c-146">The installer updates the message and ProgressBar each time it installs a reference item.</span></span>


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



