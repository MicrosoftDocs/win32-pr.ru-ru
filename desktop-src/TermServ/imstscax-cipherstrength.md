---
title: Имстскакс Циферстренгс, свойство
description: Возвращает максимальную стойкость шифрования текущего элемента управления.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Циферстренгс
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66418f2e956afcf6c5b9f1f9a0d5971119e7fddae1c1d46d115f4bbe0e6391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125445"
---
# <a name="imstscaxcipherstrength-property"></a>Свойство Имстскакс:: Циферстренгс

Возвращает максимальную стойкость шифрования текущего элемента управления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a>Значение свойства

Стойкость шифрования.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

для веб-подключение к удаленному рабочему столу стойкость шифра всегда равна 128, так как элемент управления удаленный рабочий стол ActiveX поддерживает шифрование до 128 бит. 128-разрядный элемент управления по-прежнему может подключаться к 56 разрядного шифрования удаленный рабочий стол серверов узла сеансов удаленных рабочих столов.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>См. также

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

 

 





