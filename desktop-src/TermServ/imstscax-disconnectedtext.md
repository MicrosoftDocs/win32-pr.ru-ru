---
title: Имстскакс Дисконнектедтекст, свойство
description: Задает текст, отображаемый по центру элемента управления до завершения соединения.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Дисконнектедтекст
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802746"
---
# <a name="imstscaxdisconnectedtext-property"></a>Имстскакс: свойство Исконнектедтекст:D

Задает текст, отображаемый по центру элемента управления до завершения соединения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a>Значение свойства

Новый отображаемый текст.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Установка свойства **дисконнектедтекст** является необязательной. Если он не указан, элемент управления будет пустым до установления соединения.

Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected. Метод возвращает **E \_ Fail** , если он вызывается после подключения элемента управления. Проверить, подключен ли элемент управления, можно, отреагировать на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md) или изучив свойство [**Connected**](imstscax-connected.md) .

Этот метод выделяет память, необходимую для буфера, на который указывает параметр *пдисконнектедтекст* . Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . Это не является обязательным для Visual Basic и скриптов клиентов.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиент**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**имстскакс**](imstscax-interface.md)
</dt> </dl>

 

