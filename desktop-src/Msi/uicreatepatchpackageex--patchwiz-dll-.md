---
description: Функция Уикреатепатчпаккажеекс принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет). Вызов Msimsp.exe является рекомендуемым методом для использования Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: Уикреатепатчпаккажеекс (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673165"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a>Уикреатепатчпаккажеекс (Patchwiz.dll)

Функция Уикреатепатчпаккажеекс принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет). Вызов [Msimsp.exe](msimsp-exe.md) является рекомендуемым методом для использования [Patchwiz.dll](patchwiz-dll.md).

Функция Уикреатепатчпаккажеекс доступна начиная с версии Patchwiz.dll 4,0 и расширяет функциональные возможности функции [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) .

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
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

Расположение временных файлов. Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен. Пользователь должен иметь достаточные привилегии для чтения и записи в эту папку. Расположение по умолчанию:% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*фремоветемпфолдерконтентс*
</dt> <dd>

Если **значение — true**, удалите временную папку и все ее содержимое, если оно есть. Если задано **значение false** и имеется папка, функция завершается ошибкой.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Этому параметру можно присвоить одно или несколько следующих значений, чтобы указать параметры ведения журнала или пользовательского интерфейса.



| Флаг            | Значение       | Значение                                  |
|-----------------|-------------|------------------------------------------|
| логноне         | 0x00000000  | В журнал не записываются сообщения.            |
| LOGINFO         | 0x00000001  | Запись информационных сообщений в журнал. |
| логварн         | 0x00000002  | Запись предупреждений в журнал.               |
| ложерр          | 0x00000004  | Запись сообщений об ошибках в журнал.         |
| логперфмессажес | 0x00000008  | Запись сообщений о производительности в журнал.   |
| уиноне          | 0x00000000f | Не отображать пользовательский интерфейс.       |
| уиалл           | 0x00000010  | Отображение пользовательского интерфейса.              |



 

</dd> <dt>

<span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*двресервед*
</dt> <dd>

Зарезервировано. Этот параметр должен иметь значение 0.

</dd> </dl>

## <a name="return-values"></a>Возвращаемые значения

См. таблицу в разделе [возвращаемые значения для уикреатепатчпаккаже](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Комментарии

Пример создания PCP-файла и использования [уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) для создания пакета исправлений установщик Windows см. в разделе [Пример небольшого обновления исправлений](a-small-update-patching-example.md).

Для создания исправления требуется несжатый образ установки, например административный образ или несжатый образ установки с компакт-диска. [Уикреатепатчпаккаже](uicreatepatchpackage-patchwiz-dll-.md) не создает двоичные исправления для файлов в ящиках.

 

 



