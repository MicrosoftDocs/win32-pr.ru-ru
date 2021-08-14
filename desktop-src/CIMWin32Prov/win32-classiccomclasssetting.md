---
description: Представляет параметры компонента модели COM.
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Класс Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4aa3a60b68902bbcf7728866d24e5cedd831eac35ba629a3e2516a885a28efaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418245"
---
# <a name="win32_classiccomclasssetting-class"></a>\_Класс Win32 классиккомкласссеттинг

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ классиккомкласссеттинг для Win32** представляет параметры компонента модели COM.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ классиккомкласссеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ классиккомкласссеттинг** имеет следующие свойства.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")
</dt> </dl>

Глобальный уникальный идентификатор (GUID) для COM-приложения, использующего этот COM-компонент.

</dd> <dt>

**аутоконверттоклсид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ аутоконвертто \[ Default \] ")
</dt> </dl>

Идентификатор GUID класса COM, в который будет автоматически преобразован этот COM-компонент.

</dd> <dt>

**аутотреатасклсид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ аутотреатас \[ Default \] ")
</dt> </dl>

Идентификатор GUID для COM-компонента, который будет автоматически эмулировать экземпляры этого класса.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера, \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ по умолчанию \] ")
</dt> </dl>

Идентификатор GUID этого COM-компонента.

</dd> <dt>

**Управление**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Control")
</dt> </dl>

Компонент COM является элементом управления OLE.

</dd> <dt>

**дефаултикон**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ дефаултикон \[ Default \] ")
</dt> </dl>

Путь к исполняемому файлу и идентификатору ресурса значка по умолчанию, используемого классом.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**инпрочандлер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ инпрочандлер \[ Default \] ")
</dt> </dl>

Полный путь, включая имя файла или только имя файла для 16-разрядного пользовательского обработчика COM-компонента. Поставщик не всегда возвращает полный путь.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ Default \] ")
</dt> </dl>

Полный путь, включая имя файла или только имя файла для 32-разрядного пользовательского обработчика COM-компонента. Поставщик не всегда возвращает полный путь.

</dd> <dt>

**инпроксервер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ инпроксервер \[ Default \] ")
</dt> </dl>

Полный путь, включая имя файла или только имя файла для 16-разрядного внутрипроцессного сервера DLL для этого COM-компонента. Поставщик не всегда возвращает полный путь.

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ Default \] ")
</dt> </dl>

Полный путь, включая имя файла или только имя файла для 32-разрядного внутрипроцессного сервера DLL для этого COM-компонента. Поставщик не всегда возвращает полный путь.

</dd> <dt>

**Insertable**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ inserted")
</dt> </dl>

Компонент COM можно вставить в приложения-контейнеры OLE.

</dd> <dt>

**жавакласс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ жавакласс \] ")
</dt> </dl>

Компонент COM является компонентом Java.

</dd> <dt>

**локалсервер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ локалсервер \[ Default \] ")
</dt> </dl>

Полный путь, включая имя файла или только имя файла для 16-разрядного локального серверного приложения. Поставщик не всегда возвращает полный путь.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера, \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ по умолчанию \] ")
</dt> </dl>

Полный путь, включая имя файла или только имя файла для 32-битного локального серверного приложения. Поставщик не всегда возвращает полный путь.

</dd> <dt>

**лонгдисплайнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ауксусертипе \\ \\ 3 \[ Default \] ")
</dt> </dl>

Полное имя приложения COM. Он используется в таких областях, как поле **результатов** в диалоговом окне « **Специальная вставка OLE** ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера, \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ по умолчанию \] ")
</dt> </dl>

Программный идентификатор, связанный с COM-компонентом. Формат ProgID имеет вид <Vendor. <Component. <версии. Этот идентификатор не обязательно должен быть уникальным.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ауксусертипе \\ \\ 2 \[ Default \] ")
</dt> </dl>

Короткое имя приложения COM (используется в меню и всплывающих окнах).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")
</dt> </dl>

Потоковая модель, используемая внутрипроцессный COM-классами. Если это свойство имеет **значение NULL**, то модель потоков не используется. Компонент создается в основном потоке клиента, а вызовы из других потоков маршалируются в этот поток.

Модель подразделения указывает, что компоненты могут быть указаны только одним потоком. Общие данные, удерживаемые этими типами серверов объектов, должны быть защищены от конфликтов потоков, так как объектный сервер поддерживает несколько компонентов. Каждый компонент может быть одновременно задан разными потоками.

Бесплатная модель указывает, что компоненты не накладывают ограничений на то, какие потоки или сколько потоков могут войти в этот объект. Объект не может содержать данные конкретного потока и должен защищать его данные от одновременного доступа из нескольких потоков. Доступ к компонентам с произвольным потоком, однако, не может осуществляться напрямую между апартаментными потоками, а вызовы к ним маршалируются из подразделения клиента.

Если заданы оба значения, компоненты можно использовать в режимах с потоковым апартаментом или в свободной потоке. Эти компоненты могут вводиться несколькими потоками, защищать свои данные от конфликтов потоков и не содержать данные, связанные с потоком.

Значения качества производительности:

<dl> <dd>Разделение</dd> <dd>Свободный</dd> <dd>Как</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Подразделение** ("подразделение")


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Бесплатный** ("бесплатный")


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Оба** ("оба")


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ Default \] ")
</dt> </dl>

Имя модуля и идентификатор ресурса для мелкого (16x16) точечного рисунка, используемого для кнопки панели инструментов или панели элементов. используется, если COM-компонент является элементом управления OLE или ActiveX.

</dd> <dt>

**треатасклсид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ треатас \[ Default \] ")
</dt> </dl>

Идентификатор GUID COM-компонента, который может эмулировать экземпляры этого компонента.

</dd> <dt>

**типелибрарид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ typelib \[ Default \] ")
</dt> </dl>

Идентификатор GUID для библиотеки типов для этого COM-компонента.

</dd> <dt>

**Версия**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ версия \[ по умолчанию \] ")
</dt> </dl>

Номер версии этого COM-класса.

</dd> <dt>

**версиониндепендентпрогид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ версиониндепендентпрогид \[ Default \] ")
</dt> </dl>

Идентификатор программы, который согласуется для всех версий той же программы.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ классиккомкласссеттинг** является производным от [**Win32 \_ комсеттинг**](win32-comsetting.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Комсеттинг Win32**](win32-comsetting.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

