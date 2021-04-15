---
title: Специальное имя для повышения уровня COM
description: Специальное имя для повышения прав COM позволяет приложениям, работающим под управлением учетных записей пользователей (UAC), активировать классы COM с повышенными привилегиями. Дополнительные сведения см. в разделе выделение минимальных привилегий.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488381"
---
# <a name="the-com-elevation-moniker"></a>Специальное имя для повышения уровня COM

Специальное имя для повышения прав COM позволяет приложениям, работающим под управлением учетных записей пользователей (UAC), активировать классы COM с повышенными привилегиями. Дополнительные сведения см. [в разделе выделение минимальных привилегий](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).

## <a name="when-to-use-the-elevation-moniker"></a>Когда следует использовать специальное имя для повышения прав

Специальное имя повышения прав используется для активации класса COM для выполнения определенной и ограниченной функции, требующей повышенных привилегий, таких как изменение системной даты и времени.

Для повышения прав требуется участие как класса COM, так и его клиента. Класс COM должен быть настроен для поддержки повышения прав путем добавления заметок к записи реестра, как описано в разделе требования. Клиент COM должен запросить повышение прав с помощью специального имени для повышения прав.

Специальное имя повышения прав не предназначено для обеспечения совместимости приложений. Например, если вы хотите запустить устаревшее приложение COM, например WinWord, в качестве сервера с повышенными правами, следует настроить исполняемый файл клиента COM, чтобы он требовал повышения прав, а не активировать класс устаревшего приложения с моникером повышения прав. Когда клиент COM с повышенными правами вызывает [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с помощью CLSID устаревшего приложения, его состояние перетекает в серверный процесс.

Не все функции COM совместимы с повышением прав. Функции, которые не будут работать, включают:

-   Повышение прав не происходит от клиента к удаленному COM-серверу. Если Клиент активирует удаленный COM-сервер с моникером повышения прав, сервер не будет повышен, даже если он поддерживает повышение прав.
-   Если класс COM с повышенными правами использует олицетворение во время вызова COM, это может привести к потере привилегий с повышенными правами во время олицетворения.
-   Если сервер COM с повышенными правами регистрирует класс в запущенной таблице объектов (ROT), класс не будет доступен клиентам без повышенных прав.
-   Процесс, повышенный с помощью механизма UAC, не загружает классы для каждого пользователя во время активации COM. Для приложений COM это означает, что классы COM приложения должны быть установлены в куст реестра для **\_ локального \_ компьютера hKey** , если приложение должно использоваться как с непривилегированными, так и с привилегированными учетными записями. Классы COM приложения должны быть установлены только в кусте **\_ пользователей hKey** , если приложение никогда не используется привилегированными учетными записями.
-   Перетаскивание не разрешено из без повышенных привилегий в приложения с повышенными правами.

## <a name="requirements"></a>Требования

Чтобы использовать специальное имя для повышения уровня активации COM-класса, необходимо настроить класс для запуска в качестве запускающего пользователя или удостоверения приложения активации в качестве активатора. Если класс настроен для работы с любым другим удостоверением, активация возвращает значение ошибки для выполнения \_ \_ runas \_ \_ \_ \_ .

Класс также должен иметь заметку "понятное" отображаемое имя, совместимое с многоязычным пользовательским интерфейсом (MUI). Для этого требуется следующая запись реестра:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

Если эта запись отсутствует, активация возвращает ошибку CO \_ E \_ Missing \_ . Если файл MUI отсутствует, возвращается код ошибки из функции [**реглоадмуистрингв**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) .

Кроме того, чтобы указать значок приложения, отображаемый интерфейсом пользователя UAC, добавьте следующий раздел реестра:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**Иконреференце** использует тот же формат, что и **локализедстринг**:

@*пастобинари*,*-ресаурценумбер*

Кроме того, для отображения значка COM-компонент должен быть подписан.

Класс COM также должен иметь аннотации с поддержкой LUA. Для этого требуется следующая запись реестра:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

Если эта запись отсутствует, активация возвращает ошибку CO \_ E с \_ отключенным повышением \_ .

Обратите внимание, что эти записи должны существовать \_ в \_ кусте "локальный компьютер" hKey, а не в \_ кусте hKey Current \_ User или hKey \_ Users. Это не позволяет пользователям повышать уровень классов COM, для которых они также не имеют прав на регистрацию.

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>Моникер повышения прав и пользовательский интерфейс повышения прав

Если клиент уже имеет повышенные привилегии, использование моникера повышения прав не приведет к отображению пользовательского интерфейса повышения прав.

## <a name="how-to-use-the-elevation-moniker"></a>Как использовать специальное имя для повышения прав

Моникер повышения прав — это стандартное специальное имя COM, похожее на моникеры сеанса, секции или очереди. Он направляет запрос на активацию указанному серверу с указанным уровнем возвышения. Код CLSID, который должен быть активирован, отображается в строке моникера.

Специальное имя для повышения прав поддерживает следующие маркеры уровня выполнения:

1.  Администратор
2.  Наивысшая

Для этого используется следующий синтаксис:

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

В предыдущем синтаксисе моникер New используется для возврата экземпляра COM-класса, указанного в *GUID*. Обратите внимание, что моникер "New" внутренне использует интерфейс [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) для получения объекта класса, а затем вызывает метод [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) .

Специальное имя повышения прав можно также использовать для получения объекта класса, который реализует [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Затем вызывающий объект вызывает метод [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) для получения экземпляра объекта. Для этого используется следующий синтаксис:

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>Пример кода

В следующем примере кода показано, как использовать специальное имя для повышения прав. Предполагается, что уже инициализирован COM в текущем потоке.


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



[**Привязка \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) является новым в Windows Vista. Он является производным от [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).

Единственным добавлением является поле **HWND** , **HWND**. Этот маркер представляет окно, которое станет владельцем пользовательского интерфейса повышения прав, если применимо.

Если **HWND** имеет **значение NULL**, то COM вызывает [жетактивевиндов](/windows/win32/api/winuser/nf-winuser-getactivewindow) для поиска дескриптора окна, связанного с текущим потоком. Это может произойти, если клиент является сценарием, который не может заполнить структуру [**\_ OPTS3 BIND**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) . В этом случае COM попытается использовать окно, связанное с потоком скрипта.

## <a name="over-the-shoulder-ots-elevation"></a>Повышение прав (OTS-)

Повышение прав на налево (OTS-) относится к сценарию, в котором клиент запускает COM-сервер с учетными данными администратора, а не со своими собственными. (Термин «поверх наплеча» означает, что администратор просматривает клиент, когда клиент запускает сервер.)

Этот сценарий может вызвать проблему для вызовов COM на сервере, так как сервер может не вызывать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) явным образом (т. е. программно) или неявно (то есть декларативно, с помощью реестра). Для таких серверов COM выдает дескриптор безопасности, позволяющий только САМИм, СИСТЕМным и встроенным \\ администраторам выполнять вызовы COM к серверу. Это расположение не будет работать в сценариях OTS-. Вместо этого сервер должен вызвать **CoInitializeSecurity** явно или неявно, а также указать список управления доступом, включающий в себя идентификатор безопасности и систему для интерактивной группы.

В следующем примере кода показано, как создать дескриптор безопасности (SD) с идентификатором безопасности ИНТЕРАКТИВной группы.

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

В следующем примере кода показано, как вызвать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) НЕЯВНО с SD из предыдущего примера кода:


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



В следующем примере кода показано, как явно вызвать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) с помощью УКАЗАННОГО выше SD:


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a>Разрешения COM и обязательные метки доступа

В Windows Vista введено понятие *обязательных меток доступа* в дескрипторах безопасности. Метка определяет, могут ли клиенты получить доступ к COM-объекту. Метка указывается в системном списке управления доступом (SACL) дескриптора безопасности. В Windows Vista модель COM поддерживает \_ Обязательное обозначение системы метка " \_ выполнить" \_ \_ \_ . Списки SACL в разрешениях COM игнорируются в операционных системах до Windows Vista.

Начиная с Windows Vista, dcomcnfg.exe не поддерживает изменение уровня целостности (IL) в разрешениях COM. Его необходимо задать программно.

В следующем примере кода показано, как создать дескриптор безопасности COM с меткой, которая разрешает запросы на запуск и активацию от всех клиентов с низким IL. Обратите внимание, что метки допустимы для запуска и активации, а также для вызова разрешений. Таким же, можно написать COM-сервер, который запрещает запуск, активацию или вызовы от клиентов с определенным IL. Дополнительные сведения об уровнях целостности см. в подразделе «основные сведения о механизме целостности Windows Vista» статьи общие сведения о [работе в защищенном режиме Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a>CoCreateInstance и уровни целостности

Поведение [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) изменилось в Windows Vista, чтобы не допустить, чтобы клиенты с низким IL привязать к СЕРВЕРАм com по умолчанию. Сервер должен явно разрешить такие привязки, указав список SACL. Изменения в **CoCreateInstance** выглядят следующим образом:

1.  При запуске серверного процесса COM в маркере серверного процесса задается IL-код маркера клиента или сервера, в зависимости от того, что меньше.
2.  По умолчанию COM не позволяет клиентам с низким IL привязаться к выполняющимся экземплярам любых COM-серверов. Чтобы разрешить привязку, дескриптор безопасности для запуска или активации COM-сервера должен содержать список SACL, указывающий низкую метку IL (см. предыдущий раздел для примера кода, чтобы создать такой дескриптор безопасности).

## <a name="elevated-servers-and-rot-registrations"></a>Серверы с повышенными правами и регистрации в ROT

Если сервер COM должен зарегистрироваться в запущенной таблице объектов (ROT) и разрешить любому клиенту доступ к регистрации, необходимо использовать \_ флаг ротфлагс аллованиклиент. Сервер COM "активировать как активатор" не может указать РОТФЛАГС \_ аллованиклиент, так как диспетчер управления СЛУЖБАМИ DCOM (дкомскм) принудительно проверяет подделку по этому флагу. Таким образом, в Windows Vista COM добавляет поддержку новой записи реестра, которая позволяет серверу указать, что его регистрации в таблице ROT будут доступны любому клиенту.

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

Единственным допустимым значением для этой \_ записи типа DWORD является:

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

Запись должна существовать в кусте **" \_ локальный \_ компьютер" hKey** .

Эта запись предоставляет сервер "Активация в качестве активатора" с теми же функциональными возможностями, которые РОТФЛАГС \_ аллованиклиент предоставляет для сервера запуска от имени.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Безопасность в COM](security-in-com.md)
</dt> <dt>

[Понимание принципов защищенного режима Internet Explorer и работа в нем](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 