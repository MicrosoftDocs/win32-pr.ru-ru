---
title: Свойство UserName Имстскакс
description: Указывает учетные данные имени пользователя для входа.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства имени пользователя
- Свойство UserName службы удаленных рабочих столов, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609619a012c9eea865a275bc6ee86cfc06c798ba27902636f9d5f792b8cb0dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770884"
---
# <a name="imstscaxusername-property"></a>Свойство Имстскакс:: UserName

Указывает учетные данные имени пользователя для входа.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a>Значение свойства

Новое имя пользователя.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Задавать свойство **username** необязательно. если он не указан, пользователь может указать имя пользователя, когда в процессе подключения появится диалоговое окно входа Windows.

Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected. Он возвращает **E \_ Fail** , если он вызывается при соединении элемента управления. Проверить, подключен ли элемент управления, можно, отреагировать на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md) или изучив свойство [**Connected**](imstscax-connected.md) .

Метод **получения свойства \_ username** выделяет память, необходимую для буфера, на который указывает параметр *пверсион* . Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . это не является обязательным для Visual Basic и скриптов клиентов.

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

 

