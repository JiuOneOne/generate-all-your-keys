# generate-all-your-keys
from steembase.account import PasswordKey  account = 'noisy3' password = 'P5KB2ir4BaDTeeBe5SUW16F6NYGeYSVaUBn261kDPLGGCSiNahtm' key_types = [     'posting',     'active',     'owner',     'memo',     'foo_bar' ]  for key_type in key_types:     private_key = PasswordKey(account, password, key_type).get_private_key()     public_key = private_key.pubkey      print('Private ' + key_type + ' key: ' + str(private_key))     print('Public ' + key_type + ' key: ' + str(public_key) + '\n')
