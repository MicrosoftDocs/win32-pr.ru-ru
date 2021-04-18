---
title: Имсрдпклиентнонскриптабле SendKeys, метод
description: Отправляет в элемент управления ряд нажатий клавиш. Нажатия клавиш находятся в форме кода сканирования, которая является данными клавиатуры из фактических физических ключей.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Метод SendKeys службы удаленных рабочих столов
- Метод SendKeys службы удаленных рабочих столов, интерфейс Имсрдпклиентнонскриптабле
- Службы удаленных рабочих столов интерфейса Имсрдпклиентнонскриптабле, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable2
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable2, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, метод SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491658"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>Метод Имсрдпклиентнонскриптабле:: SendKeys

Отправляет в элемент управления ряд нажатий клавиш. Нажатия клавиш находятся в форме кода сканирования, которая является данными клавиатуры из фактических физических ключей.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нумкэйс* \[ окне\]
</dt> <dd>

Количество нажатий клавиш для отправки. Максимальное число ключей, которые могут быть отправлены в одной операции, равно 20. Метод возвращает **E \_ INVALIDARG** , если этот параметр больше 20. Дополнительные сведения см. в разделе "Примечания".

</dd> <dt>

*пбаррайкэйуп* \[ окне\]
</dt> <dd>

Массив, размер которого равен *нумкэйс*. Элемент имеет **значение true** , если соответствующий ключ имеет значение up, и **false** , если соответствующий ключ не работает.

</dd> <dt>

*плкэйдата* \[ окне\]
</dt> <dd>

Массив, размер которого равен *нумкэйс*. Массив содержит данные о нажатии клавиш и соответствует значению параметра *lParam* сообщения [WM \_ KeyDown](../inputdev/wm-keydown.md) . Данные указывают число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода. Описание битов в этом массиве см. в разделе [WM \_ KeyDown](../inputdev/wm-keydown.md).

Соответствующий элемент в *пбаррайкэйуп* указывает, что ключ имеет значение up или Down.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Метод **SendKeys** не использует сочетания клавиш, сделанные локальным пользователем, с нажатиями клавиш, которые отправляет метод. Все нажатия клавиш, передаваемые в метод, отправляются в удаленный сеанс в одной атомарной последовательности.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                               |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ имсрдпклиентнонскриптабле определен как 2f079c4c-87B2-4afd-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**имсрдпклиентнонскриптабле**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[WM \_ KeyDown](../inputdev/wm-keydown.md)
</dt> </dl>

 

