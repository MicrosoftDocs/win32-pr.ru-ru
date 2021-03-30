---
description: Добавляет новый перечислитель в объект Свбемрефрешер. Этот перечислитель предназначен для всех экземпляров класса, указанных в параметре Стркласс.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Свбемрефрешер. Адденум, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820221"
---
# <a name="swbemrefresheraddenum-method"></a>Свбемрефрешер. Адденум, метод

Метод **свбемрефрешер. адденум** добавляет новый перечислитель в объект [**свбемрефрешер**](swbemrefresher.md) . Этот перечислитель предназначен для всех экземпляров класса, указанных в параметре *стркласс* .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
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

*стркласс* 
</dt> <dd>

Обязательный. Строка, содержащая класс, добавляемый в обновитель. Этот класс используется в качестве перечислителя экземпляров класса. Свойство [**index**](swbemrefreshableitem-index.md) возвращаемого [**свбемрефрешаблеитем**](swbemrefreshableitem.md) представляет индекс перечислителя в коллекции обновитель.

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

Если вызов выполнен успешно, возвращается объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) , содержащий перечислитель для всех экземпляров указанного класса.

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

 

 




