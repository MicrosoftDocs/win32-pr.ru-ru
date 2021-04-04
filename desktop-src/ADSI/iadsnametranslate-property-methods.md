---
title: Методы свойств Иадснаметранслате (iAds. h)
description: Задает свойство Часереферрал.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадснаметранслате ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989094"
---
# <a name="iadsnametranslate-property-methods"></a>Методы свойств Иадснаметранслате

Метод property интерфейса [**иадснаметранслате**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) задает свойство **часереферрал** . Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**часереферрал**
</dt> <dd> <dl>

Варианты перенаправления ссылок, как определено в [**баннерах, \_ \_ \_ перечисление ссылок**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum). Если задано отслеживание ссылок, преобразование имени выполняется для объектов, которые не принадлежат этому каталогу, и являются ссылками, возвращаемыми из прослеживания ссылок.

<dt>

Тип доступа: только для записи
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Комментарии

Параметры прослеживания ссылок применяются только при использовании [**иадснаметранслате:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) и [**Иадснаметранслате:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get). Эта функция недоступна в [**иадснаметранслате:: сетекс**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) или [**Иадснаметранслате:: жетекс**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).

Интерфейс [**иадснаметранслате**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) имеет частичную реализацию объявлений, [**\_ \_ \_ перечисление по ссылкам**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) через свойство **часереферрал** . Если свойство **часереферрал** имеет нулевое значение (0), то оно аналогично указанию **баннеров \_ \_ \_ никогда** (0). Если используется ненулевое значение, то оно аналогично указанию **баннеров \_ \_ \_ всегда** (0x60). В **иадснаметранслате** не реализованы **рекламные \_ объявления \_ \_ подчиненные** (0x20) или **баннеры \_ \_ \_** .

Включен параметр по умолчанию для прослеживания ссылок (**баннеры \_ \_ \_ всегда отслеживаются по ссылкам**). Без прослеживания ссылок можно выполнять преобразование имен для объектов, размещенных только на сервере подключенного каталога. Если вы не уверены, что нужный объект находится на указанном сервере, следует задать это свойство как **баннеры \_ \_ \_ всегда**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадснаметранслате определен как B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ОБЪЯВЛЕНИЯ \_ о \_ \_ перечислении ссылок**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**Иадснаметранслате:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**Иадснаметранслате:: Жетекс**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**Иадснаметранслате:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**Иадснаметранслате:: Сетекс**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Методы свойств интерфейса](interface-property-methods.md)
</dt> </dl>

 

 





