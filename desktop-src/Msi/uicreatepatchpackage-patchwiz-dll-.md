---
description: Функция Уикреатепатчпаккаже принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: Уикреатепатчпаккаже (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896669"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>Уикреатепатчпаккаже (Patchwiz.dll)

Функция Уикреатепатчпаккаже принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет). Вызов [Msimsp.exe](msimsp-exe.md) является рекомендуемым методом для использования [Patchwiz.dll](patchwiz-dll.md). Функция [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) доступна в версии 4,0 Patchwiz.dll и расширяет функциональные возможности функции уикреатепатчпаккаже.

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*сзпкппас*
</dt> <dd>

Полный путь к файлу свойств создания исправления (файл. PCP) для этого исправления.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*сзпатчпас*
</dt> <dd>

Полный путь к создаваемому пакету исправлений установщик Windows (MSP-файл). Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен. Если он имеет **значение NULL** или является пустой строкой, функция использует значение Патчаутпутпас в [таблице свойств (Patchwiz.dll)](properties-table-patchwiz-dll-.md).

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*сзлогпас*
</dt> <dd>

Полный путь к текстовому файлу журнала, который будет добавлен. Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*хвндстатус*
</dt> <dd>

Обработчик для окна, отображающего текст состояния. Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*сзтемпфолдер*
</dt> <dd>

Расположение временных файлов. Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен. Расположение по умолчанию:% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*фремоветемпфолдерконтентс*
</dt> <dd>

Если **значение — true**, удалите временную папку и все ее содержимое, если оно есть. Если задано **значение false** и имеется папка, функция завершается ошибкой.

</dd> </dl>

## <a name="return-values"></a>Возвращаемые значения

См. таблицу в разделе [возвращаемые значения для уикреатепатчпаккаже](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Комментарии

Пример создания PCP-файла и использования Уикреатепатчпаккаже для создания пакета исправлений установщик Windows см. в разделе [Пример небольшого обновления исправлений](a-small-update-patching-example.md).

Для создания исправления требуется несжатый образ установки, например административный образ или несжатый образ установки с компакт-диска. Уикреатепатчпаккаже не создает двоичные исправления для файлов в ящиках.

 

 



