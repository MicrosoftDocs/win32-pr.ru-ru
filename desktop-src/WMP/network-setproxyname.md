---
title: Метод Network. Сетпроксинаме
description: Метод Сетпроксинаме указывает имя прокси-сервера для использования. | Метод Network. Сетпроксинаме
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- проигрыватель Windows Media метода сетпроксинаме
- проигрыватель Windows Media метода сетпроксинаме, класс сети
- класс проигрыватель Windows Media сети, метод сетпроксинаме
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9831b25e37fd6e19b70c1ee2589736394560c97f841b5d18c3a128a82997cc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134927"
---
# <a name="networksetproxyname-method"></a>Метод Network. Сетпроксинаме

Метод **сетпроксинаме** указывает имя прокси-сервера для использования.

## <a name="syntax"></a>Синтаксис


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*протокол* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя используемого прокси-сервера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **сетпроксинаме** , чтобы указать имя прокси-сервера проигрыватель Windows Media для протокола MMS. Новое имя извлекается из ТЕКСТОВОГО элемента HTML с идентификатором ID = "имя". Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> </dl>

 

 





