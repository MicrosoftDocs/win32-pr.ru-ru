---
title: Имстскадванцедсеттингс Иконфиле, свойство
description: Указывает имя файла, содержащего данные значков, которые будут доступны при отображении клиента в полноэкранном режиме.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Иконфиле
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4700c549fa82f932ed12e3f4eeb02f2d557db3f940b394e0f2f875ac6dd7dffb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000694"
---
# <a name="imstscadvancedsettingsiconfile-property"></a>Свойство Имстскадванцедсеттингс:: Иконфиле

Указывает имя файла, содержащего данные значков, которые будут доступны при отображении клиента в полноэкранном режиме.

> [!Note]  
> это свойство не поддерживается в элементе управления ActiveX (MsRdp. ocx). Она поддерживается в библиотеке MsTscAx.dll, включенной в стандартный клиент (MsTsc.exe).

 

Это свойство доступно только на запись.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a>Значение свойства

Полный путь к файлу значка или файлу, содержащему данные значков, например DLL.

## <a name="error-codes"></a>Коды ошибок

Возвращает **\_ значение false**.

## <a name="remarks"></a>Remarks

Расширение имени файла значка — ICO.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





