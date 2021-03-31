---
title: Свойство сжатия Имстскадванцедсеттингс
description: Указывает, включено ли сжатие.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Сжатие службы удаленных рабочих столов свойств
- Сжатие службы удаленных рабочих столов свойств, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство сжатия
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988857"
---
# <a name="imstscadvancedsettingscompress-property"></a>Свойство Имстскадванцедсеттингс:: сжимать

Указывает, включено ли сжатие.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a>Значение свойства

Задайте для этого параметра значение 0, чтобы отключить сжатие, или ненулевое, чтобы включить сжатие.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

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

 

 





