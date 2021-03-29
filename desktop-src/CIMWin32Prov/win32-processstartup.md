---
description: '\_Абстрактный класс WMI Процессстартуп Win32 представляет конфигурацию запуска процесса Windows.'
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Класс Win32_ProcessStartup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8def1e7ff8e3011d5ca6c2df303818bea36eca65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141046"
---
# <a name="win32_processstartup-class"></a>\_Класс Win32 процессстартуп

Абстрактный [класс WMI](../wmisdk/retrieving-a-class.md) **\_ процессстартуп Win32** представляет конфигурацию запуска процесса Windows. Класс определяется как определение типа метода, что означает, что он используется только для передачи информации в метод [**CREATE**](create-method-in-class-win32-process.md) класса [**\_ процесса Win32**](win32-process.md) .

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ процессстартуп** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ процессстартуп** имеет следующие свойства.

<dl> <dt>

**креатефлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и функции потока \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| двкреатионфлагс")
</dt> </dl>

Дополнительные значения, управляющие классом приоритета и созданием процесса. Следующие значения создания могут быть указаны в любом сочетании, за исключением указанных.

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Отладка \_ Процесс** (1)


</dt> <dd>

Если этот флаг установлен, вызывающий процесс обрабатывается как отладчик, а новый процесс отлаживается. Система уведомляет отладчик обо всех событиях отладки, происходящих в отлаживаемом процессе.

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Отладка \_ Только \_ этот \_ процесс** (2)


</dt> <dd>

Если этот флаг не установлен и выполняется отладка вызывающего процесса, новый процесс становится еще одним отлаживаемым процессом. Если вызывающий процесс не является отлаживаемым процессом, действия, связанные с отладкой, не выполняются.

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Создание \_ Приостановлено** (4)


</dt> <dd>

Основной поток нового процесса создается в приостановленном состоянии и не выполняется до тех пор, пока не будет вызван метод [**ресумесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>Отсоединено **\_ Процесс** (8)


</dt> <dd>

Для процессов консоли новый процесс не имеет доступа к консоли родительского процесса. Этот флаг нельзя использовать, если установлен флаг **создания \_ новой \_ консоли** .

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Создание \_ Новая \_ консоль** (16)


</dt> <dd>

Этот новый процесс имеет новую консоль, а не наследует родительскую консоль. Этот флаг нельзя использовать с флагом **отсоединенного \_ процесса** .

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Создание \_ Новая \_ \_ Группа процессов** (512)


</dt> <dd>

Этот новый процесс является корневым процессом новой группы процессов. Группа процессов включает все процессы, которые являются потомками этого корневого процесса. Идентификатор процесса новой группы процессов совпадает с идентификатором процесса, возвращаемым в свойстве **ProcessID** класса [**\_ процесса Win32**](win32-process.md) . Группы процессов используются методом [**женератеконсолектрлевент**](/windows/console/generateconsolectrlevent) для включения отправки сигналов CTRL + C или Ctrl + Break в группу процессов консоли.

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Создание \_ \_Среда Юникода** (1024)


</dt> <dd>

Параметры среды, перечисленные в свойстве **EnvironmentVariables** , используют символы Юникода. Если этот флаг не установлен, блок среды использует символы ANSI.

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Создание \_ \_ \_ Режим ошибок по умолчанию** (67108864)


</dt> <dd>

Только что созданные процессы получают по умолчанию системный режим ошибок вызывающего процесса, а не наследуют режим ошибок родительского процесса. Этот флаг полезен для многопоточных приложений оболочки, которые выполняются с отключенными жесткими ошибками.

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Создание \_ БРЕАКАВАЙ \_ из \_ задания** (16777216)


</dt> <dd>

Используется, чтобы созданный процесс не был ограничен объектом задания.

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hKey \_ Текущая \_ Пользовательская \\ \\ Среда")
</dt> </dl>

Список параметров конфигурации компьютера. Переменные среды указывают пути поиска для файлов, каталоги для временных файлов, параметры конкретного приложения и другие аналогичные сведения. Система поддерживает блок параметров среды для каждого пользователя и один для компьютера. Блок системной среды представляет переменные среды для всех пользователей определенного компьютера. Блок среды пользователя представляет переменные среды, которые система поддерживает для конкретного пользователя, и включает набор системных переменных среды. По умолчанию каждый процесс получает копию блока среды для своего родительского процесса. Как правило, это блок среды для пользователя, вошедшего в систему. Процесс может указывать различные блоки среды для своих дочерних процессов.

</dd> <dt>

**ErrorMode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Error functions \| функцию SetErrorMode")
</dt> </dl>

На некоторых процессорах, отличных от x86, неправильно выровненные ссылки памяти приводят к возникновению ошибки выравнивания. Флаг « **без \_ выравнивания \_ \_** » позволяет управлять тем, будет ли операционная система автоматически исправлять такие ошибки выравнивания или сделать их видимыми для приложения. В миллионах инструкций в секунду для платформы MIPS приложение должно явным образом вызвать [**функцию SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) с параметром **без \_ выравнивания, \_ \_ Кроме** флага, чтобы операционная система автоматически исправит ошибки выравнивания.

Как операционная система обрабатывает несколько типов серьезных ошибок. Можно указать, что ошибки процесса операционной системы или приложение может принимать и обрабатывать ошибки.

Значение по умолчанию — для операционной системы, чтобы сделать ошибки выравнивания видимыми для приложения. Так как платформа x86 не делает ошибки выравнивания видимыми для приложения, неисправность **без \_ выравнивания, \_ \_ Кроме** флага, не позволяет операционной системе выдать ошибку выравнивания, даже если флаг не установлен. Состояние по умолчанию для [**функцию SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) — установка всех флагов равным 0 (нулю).

<dt>



 (1)


</dt> <dd>

Значение по умолчанию

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Не пройден \_ Критические \_ ошибки** (2)


</dt> <dd>

Если этот флаг установлен, операционная система не отображает окно сообщения о критическом обработчике ошибок при возникновении такой ошибки. Вместо этого операционная система отправляет сообщение об ошибке вызывающему процессу.

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Нет \_ Ошибка выравнивания, \_ \_ Кроме** (4)


</dt> <dd>

Если этот флаг установлен, операционная система автоматически исправляет ошибки выравнивания памяти и делает их невидимыми для приложения. Это делается для вызывающих и подчиненных процессов. Этот флаг применяется только к ограниченной инструкции SET Computing (RISC) и не влияет на процессоры x86.

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Нет \_ \_ \_ \_ Поле "ошибка сбоя GP"** (8)


</dt> <dd>

Если этот флаг установлен, операционная система не отображает окно сообщения об ошибке общей защиты (GP) при возникновении ошибки GP. Этот флаг следует устанавливать только при отладке приложений, которые обрабатывали ошибки GP.

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Нет \_ \_ \_ \_ Поле "Ошибка открытия файла"** (16)


</dt> <dd>

Если этот флаг установлен, операционная система не отображает окно сообщения, если не удается найти файл. Вместо этого в вызывающий процесс возвращается ошибка. Этот флаг в данный момент игнорируется.

</dd> </dl>

</dd> <dt>

**филлаттрибуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двфиллаттрибуте")
</dt> </dl>

Цвета текста и фона, если в консольном приложении создано новое окно консоли. Эти значения игнорируются в приложениях графического интерфейса пользователя. Чтобы указать как цвет переднего плана, так и цвет фона, добавьте значения вместе. Например, чтобы красный тип (4) был на синем фоне (16), задайте для параметра Филлаттрибуте значение 20.

<dt>

1
</dt> <dd>

Синий цвет переднего плана \_

</dd> <dt>

2
</dt> <dd>

Зеленый передний план \_

</dd> <dt>

4
</dt> <dd>

Красный передний план \_

</dd> <dt>

8
</dt> <dd>

Интенсивность переднего плана \_

</dd> <dt>

16
</dt> <dd>

\_Синий фон

</dd> <dt>

32
</dt> <dd>

\_Зеленый фон

</dd> <dt>

64
</dt> <dd>

\_Красный фон

</dd> <dt>

128
</dt> <dd>

\_Интенсивность фона

</dd> </dl>

</dd> <dt>

**PriorityClass значение**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**жобобжект \_ Basic \_ Limit \_ Information**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass значение")
</dt> </dl>

Класс приоритета нового процесса. Это свойство используется для определения приоритетов потоков в процессе. Если свойство оставлено равным null, класс приоритета по умолчанию имеет значение "Стандартный", если класс приоритета процесса создания не простаивает или не ниже \_ обычного. В таких случаях дочерний процесс получает класс приоритета по умолчанию для вызывающего процесса.

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (32)


</dt> <dd>

Обозначает нормальный процесс без специальных требований к расписанию.

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Бездействие** (64)


</dt> <dd>

Обозначает процесс с потоками, которые выполняются только в том случае, когда система бездействует и заменяется потоками любого процесса, запущенного в классе с более высоким приоритетом. Примером является экранная заставка. Класс приоритета простоя наследуется дочерними процессами.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Высокий** (128)


</dt> <dd>

Обозначает процесс, выполняющий критические по времени задачи, которые должны быть выполнены немедленно для правильной работы. Потоки процесса класса с высоким приоритетом выгружают потоки процессов класса с обычным приоритетом или с приоритетом простоя. Примером может быть Windows список задач, который должен быстро реагировать при вызове пользователем, независимо от нагрузки на операционную систему. При использовании класса с высоким приоритетом необходимо соблюдать осторожность, так как приложение класса с высоким приоритетом может использовать почти все доступные циклы. Для этого уровня задаются только потоки приоритетного прерывания в режиме реального времени.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Реальное** (256)


</dt> <dd>

Указывает процесс с наибольшим возможным приоритетом. Потоки процесса класса приоритета в реальном времени выгружают потоки всех других процессов, включая потоки с высоким приоритетом и процессы операционной системы, выполняющие важные задачи. Например, процесс в режиме реального времени, который выполняется в течение более короткого интервала, может привести к тому, что дисковые кэши не будут сбрасываться или заставить мышь не отвечать.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Ниже \_ Обычная** (16384)


</dt> <dd>

Указывает процесс с приоритетом выше, чем в режиме простоя, но ниже обычного.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Выше \_ Обычная** (32768)


</dt> <dd>

Указывает процесс с приоритетом выше обычного, но меньше высокого.

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| вшоввиндов")
</dt> </dl>

Способ отображения окна для пользователя.

<dt>

<span id="SW_HIDE"></span><span id="sw_hide"></span>

<span id="SW_HIDE"></span><span id="sw_hide"></span>**SW \_ СКРЫТЬ** (0)


</dt> <dd>

Скрывает окно и активирует другое окно.

</dd> <dt>

<span id="SW_NORMAL"></span><span id="sw_normal"></span>

<span id="SW_NORMAL"></span><span id="sw_normal"></span>**SW \_ Обычная** (1)


</dt> <dd>

Активирует и отображает окно. Если окно свернется или разворачивается, система восстанавливает исходный размер и расположение. Приложение задает этот флаг при первом отображении окна.

</dd> <dt>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**SW \_ ШОВМИНИМИЗЕД** (2)


</dt> <dd>

Активирует окно и отображает его в виде уменьшенного окна.

</dd> <dt>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**SW \_ ШОВМАКСИМИЗЕД** (3)


</dt> <dd>

Активирует окно и отображает его как развернутое окно.

</dd> <dt>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**SW \_ ШОВНОАКТИВАТЕ** (4)


</dt> <dd>

Отображает окно в самом последнем размере и положении. Это значение аналогично **\_ стандарту SW**, за исключением того, что окно не активировано.

</dd> <dt>

<span id="SW_SHOW"></span><span id="sw_show"></span>

<span id="SW_SHOW"></span><span id="sw_show"></span>**SW \_ ПОКАЗЫВАТЬ** (5)


</dt> <dd>

Активирует окно и отображает его в текущем размере и позиции.

</dd> <dt>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW \_ MINIMIZE** (6)


</dt> <dd>

Свертывает указанное окно и активирует следующее окно верхнего уровня в Z-порядке.

</dd> <dt>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**SW \_ ШОВМИННОАКТИВЕ** (7)


</dt> <dd>

Отображает окно в виде уменьшенного окна. Это значение аналогично **SW \_ шовминимзед**, за исключением того, что окно не активировано.

</dd> <dt>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW \_ Показано** (8)


</dt> <dd>

Отображает окно по текущему размеру и положению. Это значение аналогично **\_ показу SW**, за исключением того, что окно не активировано.

</dd> <dt>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>**SW \_ Восстановление** (9)


</dt> <dd>

Активирует и отображает окно. Если окно свернется или разворачивается, система восстанавливает исходный размер и расположение. Приложение задает этот флаг при восстановлении окна, которое было уменьшено.

</dd> <dt>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**SW \_ ШОВДЕФАУЛТ** (10)


</dt> <dd>

Устанавливает состояние отображения на основе значения **SW \_ \** _, указанного в структуре [_ *стартупинфо* *](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , передаваемой в функцию [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) программой, запускающей приложение.

</dd> <dt>

<span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>

<span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>**SW \_ ФОРЦЕМИНИМИЗЕ** (11)


</dt> <dd>

Свертывает окно, даже если поток, владеющий окном, перестает отвечать на запросы. Этот флаг следует использовать только при минимизации Windows из другого потока.

</dd> </dl>

</dd> <dt>

**Title**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| лптитле")
</dt> </dl>

Текст, отображаемый в строке заголовка при создании нового окна консоли; используется для процессов консоли. Если **значение равно NULL**, в качестве заголовка окна используется имя исполняемого файла. Это свойство должно иметь **значение NULL** для графических интерфейсов или консольных процессов, которые не создают новое окно консоли.

</dd> <dt>

**винстатиондесктоп**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| лпдесктоп")
</dt> </dl>

Имя рабочего стола или имя рабочего стола и станции окна для процесса. Обратная косая черта в строке указывает, что строка включает как настольные, так и оконные станции. Если **винстатиондесктоп** имеет **значение NULL**, новый процесс наследует настольную и оконную станцию своего родительского процесса. Если **винстатиондесктоп** является пустой строкой, процесс не наследует настольную и оконную станции родительского процесса. Система определяет, нужно ли создавать новую станцию рабочего стола и Windows. Оконная станция — это защищенный объект, содержащий буфер обмена, набор глобальных атомов и группу объектов настольных систем. Интерактивная экранная станция, назначенная сеансу входа интерактивного пользователя, также содержит клавиатуру, мышь и устройство вывода. Рабочий стол — это защищенный объект, содержащийся на станции Windows. Рабочий стол имеет логическую поверхность отображения и содержит окна, меню и обработчики. Станция окна может иметь несколько настольных компьютеров. Только рабочие столы интерактивной экранной станции могут быть видимыми и получать вводимые пользователем данные.

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двкс")
</dt> </dl>

Смещение по оси X верхнего левого угла окна при создании нового окна — в пикселях. Смещение находится в левом верхнем углу экрана. Для процессов графического пользовательского интерфейса указанная единица используется в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр *X* объекта **CreateWindow** имеет значение **\_ уседефаулт во Вт**.

> \[! Примечание X\]  
> и **Y** не могут быть указаны независимо друг от друга.

 

</dd> <dt>

**кскаунтчарс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| кскаунтчарс")
</dt> </dl>

Ширина буфера экрана в символьных столбцах. Это свойство используется для процессов, которые создают окно консоли и не учитывается в процессах графического пользовательского интерфейса.

> [!Note]  
> **Кскаунтчарс** и **икаунтчарс** нельзя указывать отдельно.

 

</dd> <dt>

**кссизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двкссизе")
</dt> </dl>

Ширина окна в пикселях при создании нового окна. Для процессов графического пользовательского интерфейса этот метод используется только в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр нвидс **CreateWindow** — **Вт \_ уседефаулт**.

> [!Note]  
> **Кссизе** и **исизе** нельзя указывать отдельно.

 

</dd> <dt>

**да**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| дви")
</dt> </dl>

Смещение в пикселях верхнего левого угла окна при создании нового окна. Смещение находится в левом верхнем углу экрана. Для процессов графического пользовательского интерфейса указанная единица используется в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр *y* объекта **CreateWindow** имеет значение **\_ уседефаулт во Вт**.

> \[! Примечание X\]  
> и **Y** не могут быть указаны независимо друг от друга.

 

</dd> <dt>

**икаунтчарс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| икаунтчарс")
</dt> </dl>

Высота буфера экрана в строках символов. Это свойство используется для процессов, которые создают окно консоли, но игнорируется в процессах графического пользовательского интерфейса.

> [!Note]  
> **Кскаунтчарс** и **икаунтчарс** нельзя указывать отдельно.

 

</dd> <dt>

**исизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процессов и структур потоков \| [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| двисизе")
</dt> </dl>

Высота окна в пикселях при создании нового окна. Для процессов графического пользовательского интерфейса этот метод используется только в первый раз, когда новый процесс вызывает [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для создания перекрытого окна, если параметр *Нвидс* **CreateWindow** — **Вт \_ уседефаулт**.

> [!Note]  
> **Кссизе** и **исизе** нельзя указывать отдельно.

 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот класс является производным от [**Win32 \_ месодпараметеркласс**](win32-methodparameterclass.md).

Обзор

Метод [**Win32 \_ Process**](win32-process.md) [**CREATE**](create-method-in-class-win32-process.md) позволяет настроить параметры запуска для любого нового процесса, выполняемого на компьютере. Например, можно настроить процесс, чтобы он начинался в скрытом окне, что не позволит пользователю видеть и, возможно, прерывать его. Если процесс выполняется в окне командной строки, можно настроить размер, заголовок и цвет переднего плана и фона окна.

Параметры запуска настраиваются с помощью класса **Win32 \_ процессстартуп** . **Win32 \_ Процессстартуп** является классом типа метода; класс типа метода существует только для передачи информации в метод. В этом случае все свойства экземпляра **Win32 \_ процессстартуп** передаются в экземпляр [**\_ процесса Win32**](win32-process.md).

**Использование Win32 \_ процессстартуп**

1.  Создайте экземпляр **Win32 \_ процессстартуп**.
2.  Настройте свойства нового экземпляра.
3.  Включите экземпляр как часть метода [**\_ процесса Win32**](win32-process.md) Create.

Например, если вы создали экземпляр **Win32 \_ процессстартуп** с именем обжконфиг, имя объекта необходимо передать в метод Create следующим образом:

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>Примеры

Для настройки различных параметров запуска процесса можно использовать класс **Win32 \_ процессстартуп** . Эти параметры включают, но не ограничиваются, такие вещи, как создание процесса в скрытом окне и создание процесса с более высоким приоритетом. Следующий сценарий VBScript создает процесс в скрытом окне.


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



Следующий сценарий VBScript создает процесс с более высоким приоритетом.


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



В следующем примере кода VBScript создается процесс «блокнот» на локальном компьютере. **Win32 \_ Процессстартуп** используется для настройки параметров процесса.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Месодпараметеркласс Win32**](win32-methodparameterclass.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> <dt>

[**\_Процесс Win32**](win32-process.md)
</dt> <dt>

[**\_\_провидерхосткуотаконфигуратион**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[Задачи WMI: процессы](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
