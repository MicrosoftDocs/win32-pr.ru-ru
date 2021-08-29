---
title: Метод Initialize Инапсохконструктор (Наппротокол. h)
description: Инициализирует пакет протокола SoH в системе защиты доступа к сети.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Инициализация метода NAP
- Инициализация метода NAP, интерфейс Инапсохконструктор
- Инапсохконструктор интерфейса NAP, метод Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d03d821b441aa71f4766fc255f48122fe4f2c432d60d52ab957022d7be50a79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803034"
---
# <a name="inapsohconstructorinitialize-method"></a>Метод Инапсохконструктор:: Initialize

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапсохконструктор:: Initialize** инициализирует пакет протокола SoH в системе защиты доступа к сети.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор* \[ в\]
</dt> <dd>

Уникальный [системхеалсентитид](nap-datatypes.md) , СОДЕРЖАЩИЙ идентификатор SHA или SHV, который конструирует пакет.

</dd> <dt>

*запрос* \[ окне\]
</dt> <dd>

**Логическое** **значение** , равное true, если пакет должен быть [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , и **false** , если он должен быть **сохреспонсе**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                     | Описание                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>           | Операция выполнена успешно.<br/>                                   |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl> | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>  | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод должен вызываться только один раз для каждого пакета.

[Системхеалсентитид](nap-datatypes.md) , указанный в поле *ID*, является первым TLV в новом пакете SoH и имеет тип атрибута [**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Наппротокол. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Наппротокол. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**инапсохконструктор**](inapsohconstructor.md)
</dt> </dl>

 

 





