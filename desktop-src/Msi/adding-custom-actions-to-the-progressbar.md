---
description: Настраиваемые действия могут добавлять сведения о времени и ходе выполнения в элемент управления ProgressBar. Дополнительные сведения о создании диалогового окна "Отображение действий" с ProgressBar см. в разделе Разработка элемента управления ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Добавление настраиваемых действий в ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d83dfeb806eb0ed6f1e251dd48b97911d8e0f583c8b65cb48ef0d04df059ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811064"
---
# <a name="adding-custom-actions-to-the-progressbar"></a>Добавление настраиваемых действий в ProgressBar

[Настраиваемые действия](custom-actions.md) могут добавлять сведения о времени и ходе выполнения в элемент управления [ProgressBar](progressbar-control.md) . Дополнительные сведения о создании диалогового окна "Отображение действий" с ProgressBar см. в разделе [Разработка элемента управления ProgressBar](authoring-a-progressbar-control.md).

обратите внимание, что в пакет установщик Windows необходимо добавить два настраиваемых действия, чтобы точно сообщить о времени и ходе выполнения элементу ProgressBar. Одно настраиваемое действие должно быть отложенным пользовательским действием. Это пользовательское действие должно завершить пользовательскую установку и отправить в элемент управления [ProgressBar](progressbar-control.md) объем отдельных приращений, когда установщик запустит сценарий установки. Второе настраиваемое действие должно быть немедленным настраиваемым действием, которое информирует ProgressBar о том, сколько тактов следует добавить к общему числу на этапе создания сценария для установки.

**Добавление настраиваемого действия в ProgressBar**

1.  Определите, как настраиваемое действие будет описывать ход выполнения. Например, пользовательское действие, устанавливающее разделы реестра, может отображать сообщение о ходе выполнения и обновлять компонент [ProgressBar](progressbar-control.md) каждый раз, когда установщик записывает один раздел реестра.
2.  Каждое обновление с помощью настраиваемого действия изменяет длину элемента [ProgressBar](progressbar-control.md) на постоянное приращение. Укажите или Вычислите количество тактов в каждом приращении. Как правило, изменение в элементе ProgressBar длины одного тика соответствует установке одного байта. Например, если установщик устанавливает примерно 10000 байт при записи одного раздела реестра, можно указать, что увеличивается такт 10000.
3.  Укажите или Вычислите общее число тактов, добавляемое настраиваемым действием в длину [ProgressBar](progressbar-control.md). Число тактов, добавленных настраиваемым действием, обычно вычисляется следующим образом: (шаг деления) x (число элементов). Например, если пользовательское действие записывает 10 разделов реестра, установщик установит примерно 100000 байт, поэтому установщик должен увеличить оценку итоговой общей длины ProgressBar на 100000 тактов.
    > [!Note]  
    > Для динамического вычисления пользовательское действие должно содержать раздел, который сразу же выполняется во время создания скрипта. Количество тактов, сообщаемое настраиваемым действием отложенного выполнения, должно быть равно числу тактов, добавляемых к общему количеству тактов в результате немедленного выполнения. Если это не так, оставшееся время, которое сообщает элементу управления "текст TimeRemaining", будет неточным.

     

4.  Разделите настраиваемое действие на два раздела кода: раздел, который выполняется на этапе создания скрипта, и раздел, который выполняется на этапе выполнения установки. Это можно сделать с помощью двух файлов или можно использовать один файл, выполнив условия в режиме выполнения установщика. В следующем примере используется один файл и проверяется состояние установки. Разделы примера зависят от того, находится ли установщик на этапе выполнения или создания сценария установки.
5.  Раздел, выполняемый во время создания скрипта, должен увеличить оценку итоговой общей длины элемента [ProgressBar](progressbar-control.md) на общее число тактов в настраиваемом действии. Это делается путем отправки сообщения о ходе выполнения **прогрессаддитион** .
6.  Раздел, выполняемый на этапе выполнения установки, должен настроить текст сообщения и шаблоны, чтобы информировать пользователя о действиях, выполняемых настраиваемым действием, и направить установщик на обновление элемента управления [ProgressBar](progressbar-control.md) . Например, сообщите установщику о необходимости переместить компонент ProgressBar на один шаг вперед и отправить сообщение о ходе выполнения с каждым обновлением. В этом разделе обычно есть цикл, если пользовательское действие устанавливает что-то. При каждом прохождении этого цикла установщик может установить один элемент ссылки, например раздел реестра, и обновить элемент управления ProgressBar.
7.  добавьте немедленный настраиваемое действие выполнения в пакет установщик Windows. Это пользовательское действие информирует компонент [ProgressBar](progressbar-control.md) о том, как он будет изменяться на этапах установки и создания сценариев. В следующем примере источником является библиотека DLL, созданная путем компиляции примера кода, а целевым объектом является точка входа Капрогресс.
8.  добавьте настраиваемое действие отложенного выполнения в пакет установщик Windows. Это пользовательское действие выполняет шаги фактической установки и информирует [ProgressBar](progressbar-control.md) о том, сколько времени необходимо для того, чтобы на момент запуска скрипта установки выполнялся установщик. В следующем примере источником является библиотека DLL, созданная путем компиляции примера кода, а целевым объектом является точка входа Капрогресс.
9.  Запланируйте как настраиваемые действия между [инсталлинитиализе](installinitialize-action.md) и [функции InstallFinalize](installfinalize-action.md) в таблице [инсталлексекутесекуенце](installexecutesequence-table.md) . Отложенное настраиваемое действие должно быть запланировано сразу после немедленного выполнения настраиваемого действия. Установщик не будет выполнять отложенное настраиваемое действие до выполнения скрипта.

В следующем примере показано, как можно добавить настраиваемое действие в [ProgressBar](progressbar-control.md). Источником настраиваемых действий является библиотека DLL, созданная путем компиляции образца кода, а целью обоих настраиваемых действий является точка входа Капрогресс. Этот пример не вносит никаких изменений в систему, но работает с ProgressBar так, как если бы вы устанавливали 10 элементов ссылок, размер которых составляет примерно 10 000 байт. Установщик обновляет сообщение и компонент ProgressBar при каждом установке эталонного элемента.


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



 

 



