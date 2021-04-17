---
title: Имсрдпклиентадванцедсеттингс Нумбитмапкачес, свойство
description: Данное свойство не поддерживается. | Имсрдпклиентадванцедсеттингс Нумбитмапкачес, свойство
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Нумбитмапкачес
- Службы удаленных рабочих столов свойства Нумбитмапкачес, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Нумбитмапкачес
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674627"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Нумбитмапкачес

Данное свойство не поддерживается.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a>Значение свойства

Новое число кэшей. Значение по умолчанию — 3, что приводит к наилучшей производительности.

## <a name="error-codes"></a>Коды ошибок

Возвращает **\_ значение false**.

## <a name="remarks"></a>Комментарии

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                                                                       |
| Поддержка конца сервера<br/>    | Ни одна версия не поддерживается<br/>                                                                       |
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

 

 





