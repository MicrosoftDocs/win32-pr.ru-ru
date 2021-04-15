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
# <a name="the-com-elevation-moniker"></a><span data-ttu-id="a5c85-104">Специальное имя для повышения уровня COM</span><span class="sxs-lookup"><span data-stu-id="a5c85-104">The COM Elevation Moniker</span></span>

<span data-ttu-id="a5c85-105">Специальное имя для повышения прав COM позволяет приложениям, работающим под управлением учетных записей пользователей (UAC), активировать классы COM с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="a5c85-105">The COM elevation moniker allows applications that are running under user account control (UAC) to activate COM classes with elevated privileges.</span></span> <span data-ttu-id="a5c85-106">Дополнительные сведения см. [в разделе выделение минимальных привилегий](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="a5c85-106">For more information, see [Focus on Least Privilege](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span></span>

## <a name="when-to-use-the-elevation-moniker"></a><span data-ttu-id="a5c85-107">Когда следует использовать специальное имя для повышения прав</span><span class="sxs-lookup"><span data-stu-id="a5c85-107">When to Use the Elevation Moniker</span></span>

<span data-ttu-id="a5c85-108">Специальное имя повышения прав используется для активации класса COM для выполнения определенной и ограниченной функции, требующей повышенных привилегий, таких как изменение системной даты и времени.</span><span class="sxs-lookup"><span data-stu-id="a5c85-108">The elevation moniker is used to activate a COM class to accomplish a specific and limited function that requires elevated privileges, such as changing the system date and time.</span></span>

<span data-ttu-id="a5c85-109">Для повышения прав требуется участие как класса COM, так и его клиента.</span><span class="sxs-lookup"><span data-stu-id="a5c85-109">Elevation requires participation from both a COM class and its client.</span></span> <span data-ttu-id="a5c85-110">Класс COM должен быть настроен для поддержки повышения прав путем добавления заметок к записи реестра, как описано в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a5c85-110">The COM class must be configured to support elevation by annotating its registry entry, as described in the Requirements section.</span></span> <span data-ttu-id="a5c85-111">Клиент COM должен запросить повышение прав с помощью специального имени для повышения прав.</span><span class="sxs-lookup"><span data-stu-id="a5c85-111">The COM client must request elevation by using the elevation moniker.</span></span>

<span data-ttu-id="a5c85-112">Специальное имя повышения прав не предназначено для обеспечения совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="a5c85-112">The elevation moniker is not intended to provide application compatibility.</span></span> <span data-ttu-id="a5c85-113">Например, если вы хотите запустить устаревшее приложение COM, например WinWord, в качестве сервера с повышенными правами, следует настроить исполняемый файл клиента COM, чтобы он требовал повышения прав, а не активировать класс устаревшего приложения с моникером повышения прав.</span><span class="sxs-lookup"><span data-stu-id="a5c85-113">For example, if you want to run a legacy COM application such as WinWord as an elevated server, you should configure the COM client executable to require elevation, rather than activating the legacy application's class with the elevation moniker.</span></span> <span data-ttu-id="a5c85-114">Когда клиент COM с повышенными правами вызывает [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с помощью CLSID устаревшего приложения, его состояние перетекает в серверный процесс.</span><span class="sxs-lookup"><span data-stu-id="a5c85-114">When the elevated COM client calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) using the legacy application's CLSID, the client's elevated state will flow to the server process.</span></span>

<span data-ttu-id="a5c85-115">Не все функции COM совместимы с повышением прав.</span><span class="sxs-lookup"><span data-stu-id="a5c85-115">Not all COM functionality is compatible with elevation.</span></span> <span data-ttu-id="a5c85-116">Функции, которые не будут работать, включают:</span><span class="sxs-lookup"><span data-stu-id="a5c85-116">The functionality that will not work includes:</span></span>

-   <span data-ttu-id="a5c85-117">Повышение прав не происходит от клиента к удаленному COM-серверу.</span><span class="sxs-lookup"><span data-stu-id="a5c85-117">Elevation does not flow from a client to a remote COM server.</span></span> <span data-ttu-id="a5c85-118">Если Клиент активирует удаленный COM-сервер с моникером повышения прав, сервер не будет повышен, даже если он поддерживает повышение прав.</span><span class="sxs-lookup"><span data-stu-id="a5c85-118">If a client activates a remote COM server with the elevation moniker, the server will not be elevated, even if it supports elevation.</span></span>
-   <span data-ttu-id="a5c85-119">Если класс COM с повышенными правами использует олицетворение во время вызова COM, это может привести к потере привилегий с повышенными правами во время олицетворения.</span><span class="sxs-lookup"><span data-stu-id="a5c85-119">If an elevated COM class uses impersonation during a COM call, it might lose its elevated privileges during the impersonation.</span></span>
-   <span data-ttu-id="a5c85-120">Если сервер COM с повышенными правами регистрирует класс в запущенной таблице объектов (ROT), класс не будет доступен клиентам без повышенных прав.</span><span class="sxs-lookup"><span data-stu-id="a5c85-120">If an elevated COM server registers a class in the running object table (ROT), the class will not be available to non-elevated clients.</span></span>
-   <span data-ttu-id="a5c85-121">Процесс, повышенный с помощью механизма UAC, не загружает классы для каждого пользователя во время активации COM.</span><span class="sxs-lookup"><span data-stu-id="a5c85-121">A process elevated by using the UAC mechanism does not load per-user classes during COM activations.</span></span> <span data-ttu-id="a5c85-122">Для приложений COM это означает, что классы COM приложения должны быть установлены в куст реестра для **\_ локального \_ компьютера hKey** , если приложение должно использоваться как с непривилегированными, так и с привилегированными учетными записями.</span><span class="sxs-lookup"><span data-stu-id="a5c85-122">For COM applications, this means that the application's COM classes must be installed in the **HKEY\_LOCAL\_MACHINE** registry hive if the application is to be used both by non-privileged and privileged accounts.</span></span> <span data-ttu-id="a5c85-123">Классы COM приложения должны быть установлены только в кусте **\_ пользователей hKey** , если приложение никогда не используется привилегированными учетными записями.</span><span class="sxs-lookup"><span data-stu-id="a5c85-123">The application's COM classes need only be installed in the **HKEY\_USERS** hive if the application is never used by privileged accounts.</span></span>
-   <span data-ttu-id="a5c85-124">Перетаскивание не разрешено из без повышенных привилегий в приложения с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="a5c85-124">Drag and drop is not allowed from non-elevated to elevated applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c85-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a5c85-125">Requirements</span></span>

<span data-ttu-id="a5c85-126">Чтобы использовать специальное имя для повышения уровня активации COM-класса, необходимо настроить класс для запуска в качестве запускающего пользователя или удостоверения приложения активации в качестве активатора.</span><span class="sxs-lookup"><span data-stu-id="a5c85-126">In order to use the elevation moniker to activate a COM class, the class must be configured to run as the launching user or the 'Activate as Activator' application identity.</span></span> <span data-ttu-id="a5c85-127">Если класс настроен для работы с любым другим удостоверением, активация возвращает значение ошибки для выполнения \_ \_ runas \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a5c85-127">If the class is configured to run under any other identity, the activation returns the error CO\_E\_RUNAS\_VALUE\_MUST\_BE\_AAA.</span></span>

<span data-ttu-id="a5c85-128">Класс также должен иметь заметку "понятное" отображаемое имя, совместимое с многоязычным пользовательским интерфейсом (MUI).</span><span class="sxs-lookup"><span data-stu-id="a5c85-128">The class must also be annotated with a "friendly" display name that is multilingual user interface (MUI) compatible.</span></span> <span data-ttu-id="a5c85-129">Для этого требуется следующая запись реестра:</span><span class="sxs-lookup"><span data-stu-id="a5c85-129">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

<span data-ttu-id="a5c85-130">Если эта запись отсутствует, активация возвращает ошибку CO \_ E \_ Missing \_ .</span><span class="sxs-lookup"><span data-stu-id="a5c85-130">If this entry is missing, the activation returns the error CO\_E\_MISSING\_DISPLAYNAME.</span></span> <span data-ttu-id="a5c85-131">Если файл MUI отсутствует, возвращается код ошибки из функции [**реглоадмуистрингв**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) .</span><span class="sxs-lookup"><span data-stu-id="a5c85-131">If the MUI file is missing, the error code from the [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) function is returned.</span></span>

<span data-ttu-id="a5c85-132">Кроме того, чтобы указать значок приложения, отображаемый интерфейсом пользователя UAC, добавьте следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="a5c85-132">Optionally, to specify an application icon to be displayed by the UAC user interface, add the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

<span data-ttu-id="a5c85-133">**Иконреференце** использует тот же формат, что и **локализедстринг**:</span><span class="sxs-lookup"><span data-stu-id="a5c85-133">**IconReference** uses the same format as **LocalizedString**:</span></span>

<span data-ttu-id="a5c85-134">@*пастобинари*,*-ресаурценумбер*</span><span class="sxs-lookup"><span data-stu-id="a5c85-134">@*pathtobinary*,*-resourcenumber*</span></span>

<span data-ttu-id="a5c85-135">Кроме того, для отображения значка COM-компонент должен быть подписан.</span><span class="sxs-lookup"><span data-stu-id="a5c85-135">In addition, the COM component must be signed for the icon to be displayed.</span></span>

<span data-ttu-id="a5c85-136">Класс COM также должен иметь аннотации с поддержкой LUA.</span><span class="sxs-lookup"><span data-stu-id="a5c85-136">The COM class must also be annotated as LUA-Enabled.</span></span> <span data-ttu-id="a5c85-137">Для этого требуется следующая запись реестра:</span><span class="sxs-lookup"><span data-stu-id="a5c85-137">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

<span data-ttu-id="a5c85-138">Если эта запись отсутствует, активация возвращает ошибку CO \_ E с \_ отключенным повышением \_ .</span><span class="sxs-lookup"><span data-stu-id="a5c85-138">If this entry is missing, then the activation returns the error CO\_E\_ELEVATION\_DISABLED.</span></span>

<span data-ttu-id="a5c85-139">Обратите внимание, что эти записи должны существовать \_ в \_ кусте "локальный компьютер" hKey, а не в \_ кусте hKey Current \_ User или hKey \_ Users.</span><span class="sxs-lookup"><span data-stu-id="a5c85-139">Note that these entries must exist in the HKEY\_LOCAL\_MACHINE hive, not the HKEY\_CURRENT\_USER or HKEY\_USERS hive.</span></span> <span data-ttu-id="a5c85-140">Это не позволяет пользователям повышать уровень классов COM, для которых они также не имеют прав на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="a5c85-140">This prevents users from elevating COM classes that they did not also have the privileges to register.</span></span>

## <a name="the-elevation-moniker-and-the-elevation-ui"></a><span data-ttu-id="a5c85-141">Моникер повышения прав и пользовательский интерфейс повышения прав</span><span class="sxs-lookup"><span data-stu-id="a5c85-141">The Elevation Moniker and the Elevation UI</span></span>

<span data-ttu-id="a5c85-142">Если клиент уже имеет повышенные привилегии, использование моникера повышения прав не приведет к отображению пользовательского интерфейса повышения прав.</span><span class="sxs-lookup"><span data-stu-id="a5c85-142">If the client is already elevated, using the elevation moniker will not cause the Elevation UI to display.</span></span>

## <a name="how-to-use-the-elevation-moniker"></a><span data-ttu-id="a5c85-143">Как использовать специальное имя для повышения прав</span><span class="sxs-lookup"><span data-stu-id="a5c85-143">How to Use the Elevation Moniker</span></span>

<span data-ttu-id="a5c85-144">Моникер повышения прав — это стандартное специальное имя COM, похожее на моникеры сеанса, секции или очереди.</span><span class="sxs-lookup"><span data-stu-id="a5c85-144">The elevation moniker is a standard COM moniker, similar to the session, partition, or queue monikers.</span></span> <span data-ttu-id="a5c85-145">Он направляет запрос на активацию указанному серверу с указанным уровнем возвышения.</span><span class="sxs-lookup"><span data-stu-id="a5c85-145">It directs an activation request to a specified server with the specified elevation level.</span></span> <span data-ttu-id="a5c85-146">Код CLSID, который должен быть активирован, отображается в строке моникера.</span><span class="sxs-lookup"><span data-stu-id="a5c85-146">The CLSID to be activated appears in the moniker string.</span></span>

<span data-ttu-id="a5c85-147">Специальное имя для повышения прав поддерживает следующие маркеры уровня выполнения:</span><span class="sxs-lookup"><span data-stu-id="a5c85-147">The elevation moniker supports the following Run level tokens:</span></span>

1.  <span data-ttu-id="a5c85-148">Администратор</span><span class="sxs-lookup"><span data-stu-id="a5c85-148">Administrator</span></span>
2.  <span data-ttu-id="a5c85-149">Наивысшая</span><span class="sxs-lookup"><span data-stu-id="a5c85-149">Highest</span></span>

<span data-ttu-id="a5c85-150">Для этого используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a5c85-150">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

<span data-ttu-id="a5c85-151">В предыдущем синтаксисе моникер New используется для возврата экземпляра COM-класса, указанного в *GUID*.</span><span class="sxs-lookup"><span data-stu-id="a5c85-151">The preceding syntax uses the "new" moniker to return an instance of the COM class specified by *guid*.</span></span> <span data-ttu-id="a5c85-152">Обратите внимание, что моникер "New" внутренне использует интерфейс [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) для получения объекта класса, а затем вызывает метод [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) .</span><span class="sxs-lookup"><span data-stu-id="a5c85-152">Note that the "new" moniker internally uses the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface to obtain a class object and then calls [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) on it.</span></span>

<span data-ttu-id="a5c85-153">Специальное имя повышения прав можно также использовать для получения объекта класса, который реализует [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="a5c85-153">The elevation moniker can also be used to get a class object, which implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="a5c85-154">Затем вызывающий объект вызывает метод [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) для получения экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="a5c85-154">The caller then calls [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) to get an object instance.</span></span> <span data-ttu-id="a5c85-155">Для этого используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a5c85-155">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a><span data-ttu-id="a5c85-156">Пример кода</span><span class="sxs-lookup"><span data-stu-id="a5c85-156">Sample code</span></span>

<span data-ttu-id="a5c85-157">В следующем примере кода показано, как использовать специальное имя для повышения прав.</span><span class="sxs-lookup"><span data-stu-id="a5c85-157">The following code example shows how to use the elevation moniker.</span></span> <span data-ttu-id="a5c85-158">Предполагается, что уже инициализирован COM в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="a5c85-158">It assumes that you have already initialized COM on the current thread.</span></span>


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



<span data-ttu-id="a5c85-159">[**Привязка \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) является новым в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5c85-159">[**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) is new in Windows Vista.</span></span> <span data-ttu-id="a5c85-160">Он является производным от [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span><span class="sxs-lookup"><span data-stu-id="a5c85-160">It is derived from [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span></span>

<span data-ttu-id="a5c85-161">Единственным добавлением является поле **HWND** , **HWND**.</span><span class="sxs-lookup"><span data-stu-id="a5c85-161">The only addition is an **HWND** field, **hwnd**.</span></span> <span data-ttu-id="a5c85-162">Этот маркер представляет окно, которое станет владельцем пользовательского интерфейса повышения прав, если применимо.</span><span class="sxs-lookup"><span data-stu-id="a5c85-162">This handle represents a window that becomes the owner of the Elevation UI, if applicable.</span></span>

<span data-ttu-id="a5c85-163">Если **HWND** имеет **значение NULL**, то COM вызывает [жетактивевиндов](/windows/win32/api/winuser/nf-winuser-getactivewindow) для поиска дескриптора окна, связанного с текущим потоком.</span><span class="sxs-lookup"><span data-stu-id="a5c85-163">If **hwnd** is **NULL**, COM will call [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) to find a window handle associated with the current thread.</span></span> <span data-ttu-id="a5c85-164">Это может произойти, если клиент является сценарием, который не может заполнить структуру [**\_ OPTS3 BIND**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) .</span><span class="sxs-lookup"><span data-stu-id="a5c85-164">This case might occur if the client is a script, which cannot fill in a [**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) structure.</span></span> <span data-ttu-id="a5c85-165">В этом случае COM попытается использовать окно, связанное с потоком скрипта.</span><span class="sxs-lookup"><span data-stu-id="a5c85-165">In this case, COM will try to use the window associated with the script thread.</span></span>

## <a name="over-the-shoulder-ots-elevation"></a><span data-ttu-id="a5c85-166">Повышение прав (OTS-)</span><span class="sxs-lookup"><span data-stu-id="a5c85-166">Over-The-Shoulder (OTS) Elevation</span></span>

<span data-ttu-id="a5c85-167">Повышение прав на налево (OTS-) относится к сценарию, в котором клиент запускает COM-сервер с учетными данными администратора, а не со своими собственными.</span><span class="sxs-lookup"><span data-stu-id="a5c85-167">Over-the-shoulder (OTS) elevation refers to the scenario in which a client runs a COM server with an administrator's credentials rather than his or her own.</span></span> <span data-ttu-id="a5c85-168">(Термин «поверх наплеча» означает, что администратор просматривает клиент, когда клиент запускает сервер.)</span><span class="sxs-lookup"><span data-stu-id="a5c85-168">(The term "over the shoulder" means that the administrator is watching over the client's shoulder as the client runs the server.)</span></span>

<span data-ttu-id="a5c85-169">Этот сценарий может вызвать проблему для вызовов COM на сервере, так как сервер может не вызывать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) явным образом (т. е. программно) или неявно (то есть декларативно, с помощью реестра).</span><span class="sxs-lookup"><span data-stu-id="a5c85-169">This scenario might cause a problem for COM calls into the server, because the server might not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) either explicitly (that is, programmatically) or implicitly (that is, declaratively, using the registry).</span></span> <span data-ttu-id="a5c85-170">Для таких серверов COM выдает дескриптор безопасности, позволяющий только САМИм, СИСТЕМным и встроенным \\ администраторам выполнять вызовы COM к серверу.</span><span class="sxs-lookup"><span data-stu-id="a5c85-170">For such servers, COM computes a security descriptor that allows only SELF, SYSTEM, and Builtin\\Administrators to makes COM calls into the server.</span></span> <span data-ttu-id="a5c85-171">Это расположение не будет работать в сценариях OTS-.</span><span class="sxs-lookup"><span data-stu-id="a5c85-171">This arrangement will not work in OTS scenarios.</span></span> <span data-ttu-id="a5c85-172">Вместо этого сервер должен вызвать **CoInitializeSecurity** явно или неявно, а также указать список управления доступом, включающий в себя идентификатор безопасности и систему для интерактивной группы.</span><span class="sxs-lookup"><span data-stu-id="a5c85-172">Instead, the server must call **CoInitializeSecurity**, either explicitly or implicitly, and specify an ACL that includes the INTERACTIVE group SID and SYSTEM.</span></span>

<span data-ttu-id="a5c85-173">В следующем примере кода показано, как создать дескриптор безопасности (SD) с идентификатором безопасности ИНТЕРАКТИВной группы.</span><span class="sxs-lookup"><span data-stu-id="a5c85-173">The following code example shows how to create a security descriptor (SD) with the INTERACTIVE group SID.</span></span>

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

<span data-ttu-id="a5c85-174">В следующем примере кода показано, как вызвать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) НЕЯВНО с SD из предыдущего примера кода:</span><span class="sxs-lookup"><span data-stu-id="a5c85-174">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitly with the SD from the previous code example:</span></span>


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



<span data-ttu-id="a5c85-175">В следующем примере кода показано, как явно вызвать [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) с помощью УКАЗАННОГО выше SD:</span><span class="sxs-lookup"><span data-stu-id="a5c85-175">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitly with the above SD:</span></span>


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



## <a name="com-permissions-and-mandatory-access-labels"></a><span data-ttu-id="a5c85-176">Разрешения COM и обязательные метки доступа</span><span class="sxs-lookup"><span data-stu-id="a5c85-176">COM Permissions and Mandatory Access Labels</span></span>

<span data-ttu-id="a5c85-177">В Windows Vista введено понятие *обязательных меток доступа* в дескрипторах безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5c85-177">Windows Vista introduces the notion of *mandatory access labels* in security descriptors.</span></span> <span data-ttu-id="a5c85-178">Метка определяет, могут ли клиенты получить доступ к COM-объекту.</span><span class="sxs-lookup"><span data-stu-id="a5c85-178">The label dictates whether clients can get execute access to a COM object.</span></span> <span data-ttu-id="a5c85-179">Метка указывается в системном списке управления доступом (SACL) дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5c85-179">The label is specified in the system access control list (SACL) portion of the security descriptor.</span></span> <span data-ttu-id="a5c85-180">В Windows Vista модель COM поддерживает \_ Обязательное обозначение системы метка " \_ выполнить" \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a5c85-180">In Windows Vista, COM supports the SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP label.</span></span> <span data-ttu-id="a5c85-181">Списки SACL в разрешениях COM игнорируются в операционных системах до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5c85-181">SACLs in the COM permissions are ignored on operating systems prior to Windows Vista.</span></span>

<span data-ttu-id="a5c85-182">Начиная с Windows Vista, dcomcnfg.exe не поддерживает изменение уровня целостности (IL) в разрешениях COM.</span><span class="sxs-lookup"><span data-stu-id="a5c85-182">As of Windows Vista, dcomcnfg.exe does not support changing the integrity level (IL) in COM permissions.</span></span> <span data-ttu-id="a5c85-183">Его необходимо задать программно.</span><span class="sxs-lookup"><span data-stu-id="a5c85-183">It must be set programmatically.</span></span>

<span data-ttu-id="a5c85-184">В следующем примере кода показано, как создать дескриптор безопасности COM с меткой, которая разрешает запросы на запуск и активацию от всех клиентов с низким IL.</span><span class="sxs-lookup"><span data-stu-id="a5c85-184">The following code example shows how to create a COM security descriptor with a label that allows launch/activation requests from all LOW IL clients.</span></span> <span data-ttu-id="a5c85-185">Обратите внимание, что метки допустимы для запуска и активации, а также для вызова разрешений.</span><span class="sxs-lookup"><span data-stu-id="a5c85-185">Note that the labels are valid for Launch/Activation and Call permissions.</span></span> <span data-ttu-id="a5c85-186">Таким же, можно написать COM-сервер, который запрещает запуск, активацию или вызовы от клиентов с определенным IL.</span><span class="sxs-lookup"><span data-stu-id="a5c85-186">Thus, it is possible to write a COM server that disallows launch, activation or calls from clients with a certain IL.</span></span> <span data-ttu-id="a5c85-187">Дополнительные сведения об уровнях целостности см. в подразделе «основные сведения о механизме целостности Windows Vista» статьи общие сведения о [работе в защищенном режиме Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a5c85-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span></span>


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



## <a name="cocreateinstance-and-integrity-levels"></a><span data-ttu-id="a5c85-188">CoCreateInstance и уровни целостности</span><span class="sxs-lookup"><span data-stu-id="a5c85-188">CoCreateInstance and Integrity Levels</span></span>

<span data-ttu-id="a5c85-189">Поведение [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) изменилось в Windows Vista, чтобы не допустить, чтобы клиенты с низким IL привязать к СЕРВЕРАм com по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5c85-189">The behavior of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) has changed in Windows Vista, to prevent Low IL clients from binding to COM servers by default.</span></span> <span data-ttu-id="a5c85-190">Сервер должен явно разрешить такие привязки, указав список SACL.</span><span class="sxs-lookup"><span data-stu-id="a5c85-190">The server must explicitly allow such bindings by specifying the SACL.</span></span> <span data-ttu-id="a5c85-191">Изменения в **CoCreateInstance** выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a5c85-191">The changes to **CoCreateInstance** are as follows:</span></span>

1.  <span data-ttu-id="a5c85-192">При запуске серверного процесса COM в маркере серверного процесса задается IL-код маркера клиента или сервера, в зависимости от того, что меньше.</span><span class="sxs-lookup"><span data-stu-id="a5c85-192">When launching a COM server process, the IL in the server process token is set to the client or server token IL, whichever is lower.</span></span>
2.  <span data-ttu-id="a5c85-193">По умолчанию COM не позволяет клиентам с низким IL привязаться к выполняющимся экземплярам любых COM-серверов.</span><span class="sxs-lookup"><span data-stu-id="a5c85-193">By default, COM will prevent Low IL clients from binding to running instances of any COM servers.</span></span> <span data-ttu-id="a5c85-194">Чтобы разрешить привязку, дескриптор безопасности для запуска или активации COM-сервера должен содержать список SACL, указывающий низкую метку IL (см. предыдущий раздел для примера кода, чтобы создать такой дескриптор безопасности).</span><span class="sxs-lookup"><span data-stu-id="a5c85-194">To allow the bind, a COM server's Launch/Activation security descriptor must contain a SACL that specifies the Low IL label (see the previous section for the sample code to create such a security descriptor).</span></span>

## <a name="elevated-servers-and-rot-registrations"></a><span data-ttu-id="a5c85-195">Серверы с повышенными правами и регистрации в ROT</span><span class="sxs-lookup"><span data-stu-id="a5c85-195">Elevated Servers and ROT Registrations</span></span>

<span data-ttu-id="a5c85-196">Если сервер COM должен зарегистрироваться в запущенной таблице объектов (ROT) и разрешить любому клиенту доступ к регистрации, необходимо использовать \_ флаг ротфлагс аллованиклиент.</span><span class="sxs-lookup"><span data-stu-id="a5c85-196">If a COM server wishes to register in the running object table (ROT) and allow any client to access the registration, it must use the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="a5c85-197">Сервер COM "активировать как активатор" не может указать РОТФЛАГС \_ аллованиклиент, так как диспетчер управления СЛУЖБАМИ DCOM (дкомскм) принудительно проверяет подделку по этому флагу.</span><span class="sxs-lookup"><span data-stu-id="a5c85-197">An "Activate As Activator" COM server cannot specify ROTFLAGS\_ALLOWANYCLIENT because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="a5c85-198">Таким образом, в Windows Vista COM добавляет поддержку новой записи реестра, которая позволяет серверу указать, что его регистрации в таблице ROT будут доступны любому клиенту.</span><span class="sxs-lookup"><span data-stu-id="a5c85-198">Therefore, in Windows Vista, COM adds support for a new registry entry that allows the server to stipulate that its ROT registrations be made available to any client:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

<span data-ttu-id="a5c85-199">Единственным допустимым значением для этой \_ записи типа DWORD является:</span><span class="sxs-lookup"><span data-stu-id="a5c85-199">The only valid value for this REG\_DWORD entry is:</span></span>

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

<span data-ttu-id="a5c85-200">Запись должна существовать в кусте **" \_ локальный \_ компьютер" hKey** .</span><span class="sxs-lookup"><span data-stu-id="a5c85-200">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span>

<span data-ttu-id="a5c85-201">Эта запись предоставляет сервер "Активация в качестве активатора" с теми же функциональными возможностями, которые РОТФЛАГС \_ аллованиклиент предоставляет для сервера запуска от имени.</span><span class="sxs-lookup"><span data-stu-id="a5c85-201">This entry provides an "Activate As Activator" server with the same functionality that ROTFLAGS\_ALLOWANYCLIENT provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5c85-202">См. также</span><span class="sxs-lookup"><span data-stu-id="a5c85-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5c85-203">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="a5c85-203">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="a5c85-204">Понимание принципов защищенного режима Internet Explorer и работа в нем</span><span class="sxs-lookup"><span data-stu-id="a5c85-204">Understanding and Working in Protected Mode Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 