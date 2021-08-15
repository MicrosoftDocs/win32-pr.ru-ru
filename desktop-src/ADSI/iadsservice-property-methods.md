---
title: Методы свойств Иадссервице (iAds. h)
description: Чтение и запись свойств, описанных в этом разделе.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссервице ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babbd7605b990776141d158d455e9df2aeb9864d7619158e16bab7e113f84d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690983"
---
# <a name="iadsservice-property-methods"></a>Методы свойств Иадссервице

Методы свойств интерфейса [**иадссервице**](/windows/desktop/api/Iads/nn-iads-iadsservice) считывают и записывают свойства, описанные в этом разделе. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Зависимости**
</dt> <dd> <dl>

Массив имен **BSTR** служб или групп загрузки, которые должны быть загружены для загрузки этой службы. Для записи используется синтаксис "Service:", за которым следует имя службы или Группа:, за которыми следует имя группы загрузки.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

**Отображаемое имя**
</dt> <dd> <dl>

Понятное имя службы.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

**ErrorControl**
</dt> <dd> <dl>

Действие, выполняемое в случае сбоя службы при запуске. Ниже приведены допустимые значения для этого свойства.

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\_Ошибка службы ADS — \_ \_ пропуск * * * *


</dt> <dd>

Программа запуска регистрирует ошибку, но возобновляет операцию запуска.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_ \_ обычная ошибка службы ADS \_ * * * *


</dt> <dd>

Программа запуска записывает в журнал ошибку и отображает окно сообщения, но возобновляет операцию запуска.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_Ошибка службы ADS, \_ \_ серьезная * * * *


</dt> <dd>

Программа запуска регистрирует ошибку. При запуске последней удачной конфигурации операция запуска продолжится. В противном случае система перезапускается с использованием последней удачной конфигурации.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_ \_ критическая ошибка службы ADS \_ * * * *


</dt> <dd>

Если возможно, программа запуска зарегистрирует ошибку. При запуске последней удачной конфигурации операция запуска завершается ошибкой. В противном случае система перезапускается с последней удачной конфигурацией.

</dd> </dl> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

**хосткомпутер**
</dt> <dd> <dl>

Строка ADsPath узла службы.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

**LoadOrderGroup**
</dt> <dd> <dl>

Имя группы порядка загрузки, членом которой является эта служба.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

**Путь**
</dt> <dd> <dl>

Путь и имя файла для исполняемого файла этой службы.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountName**
</dt> <dd> <dl>

Имя учетной записи, используемой этой службой для проверки подлинности при запуске.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

**сервицеаккаунтпас**
</dt> <dd> <dl>

Путь к учетной записи, указанной свойством **сервицеаккаунтпас** .

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

**ServiceType**
</dt> <dd> <dl>

Описание того, как служба представляет себя на главном компьютере. Это свойство может иметь значение 0 или быть сочетанием одного или нескольких из следующих значений.

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

\_ \_ Драйвер ядра службы ADS * * * * \_ (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

\_ \_ \_ Драйвер файловой системы ADS \_ * * * * (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

\_ \_ Собственный процесс службы ADS \_ * * * * (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

\_ \_ Общий процесс службы ADS \_ * * * * (0x00000020)


</dt> <dd></dd> </dl> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

**Тип запуска**
</dt> <dd> <dl>

Определяет, как запустить службу. Ниже приведены допустимые значения для этого свойства.

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\_Запуск службы \_ ADS \_ * * * *


</dt> <dd>

Служба — это драйвер устройства, запускаемый системным загрузчиком. Это значение допустимо только для служб драйверов.

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_ \_ Запуск системы службы ADS \_ * * * *


</dt> <dd>

Служба — это драйвер устройства, запускаемый функцией **иоинитсистем** . Это значение допустимо только для служб драйверов.

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_ \_ Автоматический запуск службы ADS \_ * * * *


</dt> <dd>

Служба будет автоматически запущена диспетчером управления службами во время запуска системы.

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_ \_ Запуск запроса службы ADS \_ * * * *


</dt> <dd>

Служба будет запущена диспетчером управления службами, когда процесс вызывает функцию [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_служба ADS \_ отключена * * * *


</dt> <dd>

Запуск службы невозможен. Попытки запустить результат службы в **службе ошибки кода ошибки \_ \_ отключены**.

</dd> </dl> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

**стартуппараметерс**
</dt> <dd> <dl>

Параметры, передаваемые в службу при запуске.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

**Версия**
</dt> <dd> <dl>

Версия службы.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как получить список всех доступных системных служб, работающих на главном компьютере, "Мойкомпьютер" вместе с расположением для поиска исполняемых файлов служб.


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадссервице определен как 68AF66E0-31CA-11CF-A98A-00AA006BC149<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадссервице**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[Методы свойств интерфейса](interface-property-methods.md)
</dt> </dl>

 

