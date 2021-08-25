---
title: Имстскакс, свойство домена
description: Указывает домен, в который входит текущий пользователь.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойств домена
- Службы удаленных рабочих столов свойств домена, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Domain
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 498098b57ef5ecb19958f6ef0e082022a92f15bab7f1fbfc74bef62d928e8726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125434"
---
# <a name="imstscaxdomain-property"></a>Имстскакс: свойство омаин:D

Указывает домен, в который входит текущий пользователь.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a>Значение свойства

Новое доменное имя.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Задание свойства **домена** является необязательным. если оно не задано, пользователь может выбрать домен, когда во время подключения появится диалоговое окно входа Windows.

Метод **Get \_ domain** выделяет память, необходимую для буфера, на который указывает параметр *пдомаин* . Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . это не является обязательным для Visual Basic и скриптов клиентов.

Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected. Он возвращает **E \_ Fail** , если он вызывается при соединении элемента управления. Проверить, подключен ли элемент управления, можно, отреагировать на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md) или изучив свойство [**Connected**](imstscax-connected.md) .

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

[**Подключен**](imstscax-connected.md)
</dt> <dt>

[**имстскакс**](imstscax-interface.md)
</dt> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

