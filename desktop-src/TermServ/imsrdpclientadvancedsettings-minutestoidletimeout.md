---
title: Имсрдпклиентадванцедсеттингс Минутестоидлетимеаут, свойство
description: Указывает максимальный период времени (в минутах), в течение которого клиент должен оставаться подключенным без ввода данных пользователем. Если указанное время истекает, элемент управления вызывает метод Имстскаксевентс Онидлетимеаутнотификатион.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Минутестоидлетимеаут
- Службы удаленных рабочих столов свойства Минутестоидлетимеаут, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Минутестоидлетимеаут
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681836"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Минутестоидлетимеаут

Указывает максимальный период времени (в минутах), в течение которого клиент должен оставаться подключенным без ввода данных пользователем. Если указанное время истекает, элемент управления вызывает метод [**имстскаксевентс:: онидлетимеаутнотификатион**](imstscaxevents-onidletimeoutnotification.md) .

Это свойство можно использовать в ситуации, когда необходимо отключить бездействующий сеанс. Например, в среде киоска.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a>Значение свойства

Новое время в минутах. Значение по умолчанию равно нулю, что отключает функцию. Максимальное значение — 240, которое представляет 4 часа.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                  |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





