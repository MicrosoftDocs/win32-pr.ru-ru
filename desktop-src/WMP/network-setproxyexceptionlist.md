---
title: Метод Network. Сетпроксексцептионлист
description: Метод Сетпроксексцептионлист задает список исключений прокси-сервера. | Метод Network. Сетпроксексцептионлист
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- проигрыватель Windows Media метода сетпроксексцептионлист
- проигрыватель Windows Media метода сетпроксексцептионлист, класс сети
- класс проигрыватель Windows Media сети, метод сетпроксексцептионлист
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf72d9c35778e965021ec31671e4e345ec2d8e281d18f9fcb16c8f2ff04d4722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647304"
---
# <a name="networksetproxyexceptionlist-method"></a>Метод Network. Сетпроксексцептионлист

Метод **сетпроксексцептионлист** задает список исключений прокси-сервера.

## <a name="syntax"></a>Синтаксис


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*протокол* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> <dt>

*список* \[ окне\]
</dt> <dd>

**Строка** , указывающая список узлов, разделенных точкой с запятой, для которых прокси-сервер пропускается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Это список компьютеров, доменов и (или) адресов, которые будут обходить прокси-сервер, если часть узла целевого URL-адреса совпадает с записью в списке.

\*Символ может использоваться в качестве подстановочного знака для списка записей. Например, \* . com будет соответствовать всем узлам в домене COM, а 67. \* будет соответствовать всем узлам в классе 67 подсети.

Этот метод не действует, если **жетпроксисеттингс** не возвращает значение 2 (использовать параметры вручную).

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **сетпроксексцептионлист** , чтобы указать список узлов, для которых прокси-сервер пропускается при использовании протокола MMS. Новый список извлекается из ТЕКСТОВОГО HTML-элемента с идентификатором ID = "КСЛИСТ". Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> </dl>

 

 





