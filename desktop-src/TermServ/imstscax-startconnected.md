---
title: Имстскакс Стартконнектед, свойство
description: Указывает, будет ли элемент управления устанавливать подключение к серверу узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) сразу после запуска.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Стартконнектед
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bdae5535d079335354306e47ed8378fa09450d9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880059"
---
# <a name="imstscaxstartconnected-property"></a>Свойство Имстскакс:: Стартконнектед

Указывает, будет ли элемент управления устанавливать подключение к серверу узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) сразу после запуска.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a>Значение свойства

Задайте для этого параметра **значение true** , если элемент управления должен сразу же подключаться при запуске, или **false** в противном случае.

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Это свойство наиболее полезно, когда свойства элемента управления задаются в списке параметров &lt; &gt; тега объекта, а не через вызовы скриптов.

Это свойство может использоваться, только если имя сервера указано также с помощью свойства сервера. Этот параметр должен быть задан перед запуском элемента управления, например путем включения его в список параметров &lt; &gt; тега объекта при использовании элемента управления на веб-странице.

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

[внедрение элемента управления удаленный рабочий стол ActiveX на веб-страницу](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[**имстскакс**](imstscax-interface.md)
</dt> </dl>

 

 





