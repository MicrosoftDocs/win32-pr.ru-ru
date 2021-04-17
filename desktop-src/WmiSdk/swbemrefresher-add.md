---
description: Метод Свбемрефрешер. Add добавляет новый объект Свбемрефрешаблеитем в коллекцию в объекте Свбемрефрешер. Свбемрефрешаблеитем объект в коллекцию в объекте Свбемрефрешер.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Метод Свбемрефрешер. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703443"
---
# <a name="swbemrefresheradd-method"></a>Свбемрефрешер. Add, метод

Метод **свбемрефрешер. Add** добавляет новый объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) в коллекцию в объекте [**свбемрефрешер**](swbemrefresher.md) .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсервице* 
</dt> <dd>

Обязательный. Объект [**SwbemServices**](swbemservices.md) , представляющий соединение с пространством имен, в котором находится объект, добавляемый в обновитель.

</dd> <dt>

*стринстанцепас* 
</dt> <dd>

Обязательный. Строка, содержащая относительный путь к объекту в пространстве имен. Путь должен содержать экземпляр. Свойство [**index**](swbemrefreshableitem-index.md) возвращаемого [**свбемрефрешаблеитем**](swbemrefreshableitem.md) представляет индекс объекта в коллекции обновитель.

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Строка, содержащая путь к объекту, для которого выполняется метод.

</dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если вызов выполнен успешно, возвращается объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) , содержащий один обновляемый объект.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМРЕФРЕШЕР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемрефрешер<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемрефрешер**](swbemrefresher.md)
</dt> </dl>

 

 




