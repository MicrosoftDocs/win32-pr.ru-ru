---
description: '&Win32 \_ нетворклогинпрофиле \# 8194; Класс WMI представляет данные сетевого входа конкретного пользователя в компьютерной системе, на которой работает Windows.'
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Класс Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fb71b27093cb1011b9aebaadf0a6760124b64f9e13ae7b5ef46f5ffc478cce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972654"
---
# <a name="win32_networkloginprofile-class"></a>\_Класс Win32 нетворклогинпрофиле

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ нетворклогинпрофиле для Win32** представляет данные сетевого входа конкретного пользователя в компьютерной системе, на которой работает Windows. Сюда входят, но не ограничиваются состояние пароля, права доступа, дисковые квоты и пути к каталогам входа.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ нетворклогинпрофиле** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ нетворклогинпрофиле** имеет следующие свойства.

<dl> <dt>

**AccountExpires**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ acct \_ Expires")
</dt> </dl>

Срок действия учетной записи истечет. Это значение вычисляется на основе числа секунд, истекших с 00:00:00 1 января 1970, и задается в следующем формате: YYYYMMDDHHMMSS. мммммм сутк.

Пример: 20521201000230,000000 000

</dd> <dt>

**аусоризатионфлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ flags проверки подлинности \_ "), [**битвалуес**](../wmisdk/standard-qualifiers.md) ("принтер", "связь", "сервер", "учетные записи")
</dt> </dl>

Набор флагов, указывающих ресурсы, которые пользователь имеет право использовать или изменять.

<dt>

1 (0x1)
</dt> <dd>

Принтерный

</dd> <dt>

2 (0x2)
</dt> <dd>

Взаимодействие

</dd> <dt>

4 (0x4)
</dt> <dd>

Сервер

</dd> <dt>

8 (0x8)
</dt> <dd>

Учетные записи

</dd> </dl>

</dd> <dt>

**BadPasswordCount**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management functions \| нетусеренум")
</dt> </dl>

Количество неудачных попыток ввода пароля при входе в систему компьютера, на котором работает Windows.

Пример: 0

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ кодовая \_ Страница")
</dt> </dl>

Кодовая страница для выбранного языка пользователя. Кодовая страница — это используемая кодировка.

</dd> <dt>

**Комментарий**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")
</dt> </dl>

Комментарий или описание для этого профиля входа.

</dd> <dt>

**каунтрикоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ код страны")
</dt> </dl>

Код страны или региона для выбранного языка пользователя.

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

**Флаги**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**битвалуес**](../wmisdk/standard-qualifiers.md) ("сценарий", "учетная запись отключена", "Корневая папка обязательна", "Блокировка", "пароль не требуется", "пасвворд не может изменить", "разрешен зашифрованный тестовый пароль", "временная повторяющаяся учетная запись", "Обычная учетная записи", "учетная запись междоменного доверия", "учетная запись доверия рабочей станции", "учетная запись доверия сервера", "не срок действия пароля", "учетная запись MNS", "требуемая смарт-карта", "доверенный для делегирования", "не делегировано", "использовать только ключ DES", "не требовать предварительной проверки", "срок действия пароля истек")
</dt> </dl>

Свойства, доступные для этого сетевого профиля.

К свойствам, которые можно задать, относятся:

<dt>

1 (0x1)
</dt> <dd>

Сценарий

Выполнен сценарий входа. Это значение должно быть установлено для LAN Manager 2,0.

</dd> <dt>

2 (0x2)
</dt> <dd>

Учетная запись отключена

Учетная запись пользователя отключена.

</dd> <dt>

8 (0x8)
</dt> <dd>

Требуется домашний каталог

Требуется домашний каталог.

</dd> <dt>

16 (0x10)
</dt> <dd>

Блокирование

Учетная запись в данный момент заблокирована. Для [**нетусерсетинфо**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo)это значение можно снять, чтобы разблокировать ранее заблокированную учетную запись. Это значение нельзя использовать для блокировки ранее незаблокированной учетной записи.

</dd> <dt>

32 (0x20)
</dt> <dd>

Пароль не требуется

Пароль не требуется.

</dd> <dt>

64 (0x40)
</dt> <dd>

Пароль не может быть изменен

Пользователь не может изменить пароль.

</dd> <dt>

128 (0x80)
</dt> <dd>

Зашифрованный тестовый пароль разрешен

</dd> <dt>

256 (0x100)
</dt> <dd>

Временная повторяющаяся учетная запись

Учетная запись для пользователей, Главная учетная запись которых находится в другом домене. Эта учетная запись предоставляет пользователю доступ к этому домену, но не к домену, который доверяет данному домену. Диспетчер пользователей ссылается на этот тип учетной записи в качестве учетной записи локального пользователя.

</dd> <dt>

512 (0x200)
</dt> <dd>

Обычная учетная запись

Тип учетной записи по умолчанию, представляющий обычного пользователя.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Учетная запись междоменного доверия

Разрешение на учетную запись доверия для домена, который доверяет другим доменам.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Учетная запись доверия рабочей станции

учетная запись компьютера для Windows рабочей станции или сервера, который является членом этого домена.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Учетная запись доверия сервера

Учетная запись компьютера для резервного контроллера домена, который является членом этого домена.

</dd> <dt>

65536 (0x10000)
</dt> <dd>

Срок действия пароля не истек

</dd> <dt>

131072 (0x20000)
</dt> <dd>

Учетная запись MNS

Тип учетной записи входа в набор узлов большинства (MNS), представляющий пользователя MNS.

</dd> <dt>

262144 (0x40000)
</dt> <dd>

Требуется смарт-карта

</dd> <dt>

524288 (0x80000)
</dt> <dd>

Доверенный для делегирования

</dd> <dt>

1048576 (0x100000)
</dt> <dd>

Не делегировано

</dd> <dt>

2097152 (0x200000)
</dt> <dd>

Использовать только ключ DES

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

Не требовать предварительной разработки

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Срок действия пароля истек

Указывает, что срок действия пароля истек.

</dd> </dl>

Следующие свойства описывают тип учетной записи. Можно задать только одно значение:

-   \_Обычная \_ учетная запись УФ
-   УФ \_ временная \_ \_ учетная запись повторения
-   \_ \_ учетная запись доверия рабочей станции УФ \_
-   \_ \_ \_ учетная запись доверия сервера УФ
-   \_ \_ учетная запись междоменного доверия УФ \_

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ полное \_ имя")
</dt> </dl>

Полное имя пользователя, принадлежащего профилю сетевого входа. Эта строка может быть пустой, если пользователь решает не связывать полное имя с именем пользователя.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ корневая \_ Папка")
</dt> </dl>

Путь к домашнему каталогу пользователя. Эта строка может быть пустой, если пользователь решил не указывать домашний каталог.

Пример: " \\ хомедир"

</dd> <dt>

**хомедиректоридриве**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")
</dt> </dl>

Буква диска, назначенная домашнему каталогу пользователя для входа в систему.

Пример: "C:"

</dd> <dt>

**ластлогофф**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ последний \_ Выход ")
</dt> </dl>

Последнее выход пользователя из системы. Это значение вычисляется на основе числа секунд, прошедших с 00:00:00 1 января 1970 г. Значение " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " означает, что время последнего выхода из системы неизвестно. Это значение имеет формат YYYYMMDDHHMMSS. мммммм сутк. Сведения о переводе этого свойства в местное время см. в разделе [задачи WMI: даты и время](../wmisdk/wmi-tasks--dates-and-times.md).

Пример: 19521201000230,000000 000

</dd> <dt>

**ластлогон**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ прошлый \_ Вход")
</dt> </dl>

Последний пользователь вошел в систему. Это значение вычисляется на основе числа секунд, прошедших с 00:00:00 1 января 1970 г. Это значение имеет формат YYYYMMDDHHMMSS. мммммм сутк. Сведения о переводе этого свойства в местное время см. в разделе [задачи WMI: даты и время](../wmisdk/wmi-tasks--dates-and-times.md).

Пример: 19521201000230,000000 000

</dd> <dt>

**логонхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (147), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ hours")
</dt> </dl>

Раз в неделю, когда пользователь может войти в систему. Каждый бит представляет единицу времени, заданную свойством **унитспервик** . Например, если единицей времени является час, первый бит (бит 0, слово 0) — воскресенье, 0:00 – 0:59, второй бит (бит 1, слово 0) — воскресенье, 1:00 — 1:59 и т. д. Если этому члену присвоено **значение NULL**, ограничение времени отсутствует. Время устанавливается в формате GMT и должно быть скорректировано для других часовых поясов (например, GMT минус 8 часов для PST).

</dd> <dt>

**логонсервер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ logon \_ Server")
</dt> </dl>

Имя сервера, на который отправляются запросы на вход. Именам серверов должны предшествовать две обратные косые черты ( \\ \\ ). Имя сервера со звездочкой ( \\ \\ \* ) указывает на то, что запрос на вход может обрабатываться любым сервером входа. Строка NULL указывает, что запросы отправляются на контроллер домена.

Пример: " \\ \\ MyServer"

</dd> <dt>

**максимумстораже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Максимальный объем свободного места на диске, доступный пользователю. Если Максимумстораже имеет значение USER \_ максстораже \_ ununlimited, то пользователю будет разрешено использовать все доступное место на диске.

Пример: 10000000

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сетевое управление структуры управления \| [**\_ сведениями о пользователях \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ имя")
</dt> </dl>

Учетная запись пользователя в определенном домене или компьютере. Число символов в имени не может превышать значение УНЛЕН.

Пример: "somedomain \\ JohnDoe"

</dd> <dt>

**нумберофлогонс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ NUM \_ logon")
</dt> </dl>

Количество успешных попыток входа пользователя в эту учетную запись. Значение 0xFFFFFFFF указывает, что значение неизвестно. Это свойство хранится отдельно на каждом резервном контроллере домена (BDC) в домене. Чтобы получить точное значение, следует использовать только самое большое значение из всех BDC.

Пример: 4

</dd> <dt>

**Параметры**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ пармс")
</dt> </dl>

Пространство, заданное для использования приложениями. Эта строка может иметь значение null или содержать любое число символов перед завершающим нулевым символом. Продукты Майкрософт используют этот элемент для хранения сведений о конфигурации пользователя. Не изменяйте эти сведения, так как это значение характерно для приложения.

</dd> <dt>

**Пароль**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ пароль \_ ")
</dt> </dl>

Срок действия пароля. Это значение измеряется из числа секунд, прошедшего с момента последнего изменения пароля.

Пример: 00001201000230,000000 000

</dd> <dt>

**пассвордекспирес**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**пользовательские \_ модальные \_ данные \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ Age ")
</dt> </dl>

Дата и время истечения срока действия пароля. Значение задается в следующем формате: YYYYMMDDHHMMSS. мммммм сутк

Пример: 19521201000230,000000 000

</dd> <dt>

**примариграупид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ идентификатор основной группы \_ ")
</dt> </dl>

Относительный идентификатор (RID) основной глобальной группы для этого пользователя. Идентификатор проверяет основную группу, к которой принадлежит профиль пользователя.

</dd> <dt>

**Привилегии**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Priv")
</dt> </dl>

Уровень привилегий, назначенный свойству **usri3 \_ Name** .

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

**Гость** (0)


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

**Пользователь** (1)


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

**Администратор** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Профиль**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Profile")
</dt> </dl>

Путь к профилю пользователя. Это значение может быть пустой строкой, локальным абсолютным путем или UNC-путем. Профиль пользователя содержит параметры, настраиваемые для каждого пользователя, например цвета рабочего стола.

Пример: "C: \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ путь к скрипту usri3 \_ ")
</dt> </dl>

Путь к каталогу для сценария входа пользователя. Сценарий входа автоматически выполняет набор команд при каждом входе пользователя в систему.

Пример: "C: \\ Win \\ Profiles \\ сомасстевен"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**унитспервик**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ единицы \_ в \_ неделю")
</dt> </dl>

Количество единиц времени, на которое делится неделя. Он используется со свойством **логонхаурс** для ограничения доступа пользователя к компьютеру.

Пример: 168 (ч в неделю)

</dd> <dt>

**усеркоммент**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**пользователя \_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment ")
</dt> </dl>

Определенный пользователем комментарий или описание для этого профиля.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ ID пользователя")
</dt> </dl>

RID пользователя. Идентификатор проверяет, существует ли пользователь и уникален для этого домена.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags")
</dt> </dl>

Тип учетной записи, к которой у пользователя есть права.

Значения качества производительности:

-   "Обычная учетная запись"
-   "Дублировать учетную запись"
-   "Учетная запись доверия рабочей станции"
-   "Учетная запись доверия сервера"
-   "Учетная запись междоменного доверия"
-   Неизвестный

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Обычная учетная запись** ("Обычная учетная запись")


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Повторяющаяся учетная запись** ("повторяющаяся учетная запись")


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**Учетная запись доверия рабочей станции** ("учетная запись доверия рабочей станции")


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Учетная запись доверия сервера** ("учетная запись доверия сервера")


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Учетная запись междоменного доверия** ("учетная запись междоменного доверия")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> </dl>

</dd> <dt>

**Рабочих станций**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| структуры управления сетями \| [**\_ сведения о пользователе \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Workstations")
</dt> </dl>

Имена рабочих станций, с которых пользователь может выполнять вход. Можно указать до восьми рабочих станций. имена должны быть разделены запятыми (,). Пустая строка указывает на отсутствие ограничений. Чтобы отключить вход от всех рабочих станций к этой учетной записи, задайте \_ АККАУНТДИСАБЛЕ УФ в свойстве **flags** этого класса.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ нетворклогинпрофиле** является производным от [**\_ параметра CIM**](cim-setting.md).

вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ NAME** на компьютере, где размещается реестр. Дополнительные сведения см. в разделе [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).

## <a name="examples"></a>Примеры

Пример " [список профилей входа в сеть](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) " PowerShell возвращает данные сетевого входа для всех пользователей компьютера.

Следующий пример на языке VBScript возвращает данные сетевого входа.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
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

[**\_Параметр CIM**](cim-setting.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
