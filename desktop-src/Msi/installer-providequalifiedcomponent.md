---
description: Метод Провидекуалифиедкомпонент объекта Installer возвращает полный путь к компоненту и выполняет все необходимые установки. При необходимости этот метод запрашивает источник и увеличивает счетчик использования для функции.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Метод Installer. Провидекуалифиедкомпонент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651983"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Метод Installer. Провидекуалифиедкомпонент

Метод **провидекуалифиедкомпонент** объекта [**Installer**](installer-object.md) возвращает полный путь к компоненту и выполняет все необходимые установки. При необходимости этот метод запрашивает источник и увеличивает счетчик использования для функции.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Категория* 
</dt> <dd>

Указывает идентификатор компонента для запрошенного компонента. Это может быть не GUID самого компонента, а сервера, который предоставляет правильные функциональные возможности, как в столбце ComponentId [таблицы публишкомпонент](publishcomponent-table.md).

</dd> <dt>

*Квалификатор* 
</dt> <dd>

Указывает квалификатор в списке компонентов рекламы (из [таблицы публишкомпонент](publishcomponent-table.md)).

</dd> <dt>

*InstallMode* 
</dt> <dd>

Определяет режим установки. Этот параметр может принимать одно из значений, приведенных в следующей таблице.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Значение                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**мсиинсталлмодедефаулт**</dt> <dt>0</dt> </dl>                                                                                 | Предоставляет компонент, выполняющий необходимую установку.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**мсиинсталлмодиксистинг**</dt> <dt>— 1</dt> </dl>                                                                            | Предоставляет компонент только в том случае, если компонент существует. в противном случае возвращает пустую строку. Этот режим проверяет существование файла ключа компонента.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**мсиинсталлмоденодетектион**</dt> <dt>– 2</dt> </dl>                                                                | Предоставляет компонент только в том случае, если компонент существует. в противном случае возвращает пустую строку. Этот режим проверяет, что компонент зарегистрирован, но не проверяет существование файла ключа компонента.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**мсиинсталлмоденосаурцересолутион**</dt> <dt>– 3</dt> </dl>                                    | Предоставляет путь к компоненту только в том случае, если компонент существует с параметром InstallState параметра *мсиинсталлстателокал*. При этом проверяется регистрация компонента, но не проверяется наличие файла ключа компонента.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**сочетание флагов мсиреинсталлмоде**</dt> <dt></dt> </dl> | Вызывает [**реинсталлфеатуре**](installer-reinstallfeature.md) для переустановки компонента с помощью этого параметра для параметра *ReinstallMode* , а затем предоставляет компонент.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсипровидекуалифиедкомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




