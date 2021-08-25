---
title: Имстскнонскриптабле Клеартекстпассворд, свойство
description: задает удаленный рабочий стол пароль управления ActiveX в виде открытого текста.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс Имстскнонскриптабле
- Службы удаленных рабочих столов интерфейса Имстскнонскриптабле, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс Имсрдпклиентнонскриптабле
- Службы удаленных рабочих столов интерфейса Имсрдпклиентнонскриптабле, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable2
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable2, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Клеартекстпассворд
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0519e7379eab529cc5275c85a11116764417d524a03dff2e1eab74a914b6560b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125054"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>Свойство Имстскнонскриптабле:: Клеартекстпассворд

задает удаленный рабочий стол пароль управления ActiveX в виде открытого текста.

Это свойство доступно только на запись.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Значение свойства

Пароль, используемый для подключения, указанный в текстовом формате.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Пароль передается на сервер в безопасно зашифрованном канале связи RDP. После установки пароля в виде открытого текста он не может быть получен в виде обычного текста.

свойство **клеартекстпассворд** может быть задано только в том случае, если элемент управления ActiveX удаленный рабочий стол не находится в состоянии connected. Установка этого свойства завершается ошибкой, если элемент управления подключен. Чтобы проверить состояние Connected, извлеките свойство [**имстскакс:: Connected**](imstscax-connected.md) .

Этот метод также можно вызвать для установки пароля в виде открытого текста перед его преобразованием в переносимый закодированный пароль или в двоичный (непреобразуемый) пароль. Обратите внимание, что зашифрованные пароли не должны считаться безопасными.

При первом вызове этого метода для задания пароля в формате обычного текста можно преобразовать пароль в формат Encoded.

**Преобразование пароля в формате обычного текста в закодированный формат**

1.  Задайте пароль в формате обычного текста в свойстве **клеартекстпассворд** .
2.  Чтобы получить пароль в двоичном (незакодированном) формате в кодировке, извлеките свойство [**бинарипассворд**](imstscnonscriptable-binarypassword.md) и свойства [**бинарисалт**](imstscnonscriptable-binarysalt.md) . Для задания пароля в двоичном кодированном формате требуется как часть закодированного пароля, так и часть соли.
3.  Чтобы получить пароль в переносимом кодированном формате, извлеките метод [**портаблепассворд**](imstscnonscriptable-portablepassword.md) и свойства [**портаблесалт**](imstscnonscriptable-portablesalt.md) . Обе части необходимы для установки пароля в переносимом кодированном формате.

После выполнения предыдущих трех шагов можно задать пароль в закодированном формате, задав свойства [**бинарипассворд**](imstscnonscriptable-binarypassword.md) и [**бинарисалт**](imstscnonscriptable-binarysalt.md) , а также свойства [**портаблепассворд**](imstscnonscriptable-portablepassword.md) и [**портаблесалт**](imstscnonscriptable-portablesalt.md) . Требуются обе части.

Чтобы включить автоматический вход в систему, необходимо также задать свойства [**username**](imstscax-username.md) и [**domain**](imstscax-domain.md) . если пароль не проходит проверку подлинности пользователя, то на сервере отображается диалоговое окно входа Windows, предлагающее пользователю ввести пароль.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскнонскриптабле определен как c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиентнонскриптабле**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**имстскнонскриптабле**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





