---
title: Ивмпнетворк Сетпроксексцептионлист, метод
description: Метод Сетпроксексцептионлист задает список исключений прокси-сервера. | Ивмпнетворк Сетпроксексцептионлист, метод
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- проигрыватель Windows Media метода сетпроксексцептионлист
- проигрыватель Windows Media метода сетпроксексцептионлист, интерфейс ивмпнетворк
- проигрыватель Windows Media интерфейса ивмпнетворк, метод сетпроксексцептионлист
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddfd3ce8495c02fc6ae352f918349ff7174afb99e69d9e1ba8aa19c45d1a49d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745766"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a>Метод Ивмпнетворк:: Сетпроксексцептионлист

Метод **сетпроксексцептионлист** задает список исключений прокси-сервера.

## <a name="syntax"></a>Синтаксис


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрпротокол* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем протокола. Список поддерживаемых протоколов см. в разделе [Поддерживаемые протоколы и типы файлов](supported-protocols-and-file-types.md).

</dd> <dt>

*пбстрексцептионлист* \[ окне\]
</dt> <dd>

**Строка System. String** , которая представляет собой разделенный точками с запятой список узлов, для которых прокси-сервер пропускается. Начальные и конечные пробелы не должны присутствовать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Это список компьютеров, доменов и (или) адресов, которые будут обходить прокси-сервер, если часть узла целевого URL-адреса совпадает с записью в списке.

\*Символ может использоваться в качестве подстановочного знака для записи списка. Например, \* . com будет соответствовать всем узлам в домене COM, а 67. \* будет соответствовать всем узлам в классе 67 подсети.

Этот метод не действует, если значение, полученное из **ивмпнетворк. жетпроксисеттингс** , равно 2 (используйте параметры вручную).

Этот метод завершается ошибкой, если вызывающее приложение не выполняется на локальном компьютере или в интрасети.

## <a name="examples"></a>Примеры

В следующем примере кода используется **сетпроксексцептионлист** для указания списка узлов, для которых прокси-сервер пропускается при использовании протокола MMS. Новый список извлекается из текстового поля при нажатии кнопки. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпнетворк (VB и C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Ивмпнетворк. Жетпроксексцептионлист (VB и C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[**Ивмпнетворк. Жетпроксисеттингс (VB и C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





